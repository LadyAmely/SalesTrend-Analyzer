<template>
  <div class="dashboard">

    <div class="header">
      <button @click="toggleSidebar" class="toggle-btn">  <i class="fas fa-bars"></i> </button>
      <a href="#" class="logo">Sale Trend Analyzer</a>
      <div class="nav-links">
        <a href="#features">Features</a>
        <a href="#pricing">Pricing</a>
        <a href="#contact">Contact</a>
      </div>
      <div class="actions">
        <i class="fas fa-search action-btn"></i>
        <i class="fas fa-cog action-btn"></i>
        <i class="fas fa-user action-btn"></i>
      </div>
    </div>


    <transition name="slide">
      <div v-if="isSidebarOpen" class="sidebar">
       <h3>Sales Insights</h3>
        <ul>
          <li><a href="#dashboard"><i class="fas fa-th-large"></i>Dashboard</a></li>
          <li><a href="#sales-overview"><i class="fas fa-chart-line"></i>Sales Overview</a></li>
          <li><a href="#trend-analysis"><i class="fas fa-chart-bar"></i>Trend Analysis</a></li>
          <li><a href="#reports"><i class="far fa-file"></i> Reports</a></li>
          <li><a href="#forecasting"><i class="far fa-calendar"></i> Forecasting</a></li>
          <li><a href="#settings"><i class="fas fa-sliders-h"></i> Settings</a></li>
          <li><a href="#help & support"><i class="far fa-question-circle"></i> Help & Support</a></li>
          <li><a href="#logout"><i class="fas fa-sign-out-alt"></i>Logout</a></li>
        </ul>
        <div class="sidebar-footer">
          <p>Powered by Lady Amely</p>
          <p>Contact Me</p>
          <p>
            <a href="https://www.facebook.com/yourprofile" class="social-icons"><i class="fab fa-facebook-f"></i></a>
            <a href="https://www.instagram.com/yourprofile" class="social-icons"><i class="fab fa-instagram"></i></a>
            <a href="https://www.linkedin.com/in/yourprofile" class="social-icons"><i class="fab fa-linkedin-in"></i></a>
          </p>
        </div>
      </div>
    </transition>

    <div class="content">

        <h1>Sales Dashboard</h1>

      <div class="kpis">
        <div class="kpi">
          <h3>Today's Sales</h3>
          <p>$5,000</p>
        </div>
        <div class="kpi-week">
          <h3>Sales This Week</h3>
          <p>$35,000</p>
        </div>
        <div class="kpi-month">
          <h3>Sales This Month</h3>
          <p>$150,000</p>
        </div>
        <div class="kpi-total">
          <h3>Total Sales</h3>
          <p>$1,500,000</p>
        </div>
        <div class="kpi-average">
          <h3>Average Order Value</h3>
          <p>$120</p>
        </div>
        <div class="kpi-new-customer">
          <h3>New Customers</h3>
          <p>50</p>
        </div>
      </div>


      <div class="transactions">
        <h3>Recent Transactions</h3>
        <table>
          <thead>
          <tr>
            <th>Date</th>
            <th>Customer</th>
            <th>Product</th>
            <th>Quantity</th>
            <th>Price</th>
            <th>Total</th>
          </tr>
          </thead>
          <tbody>
          <tr>
            <td>2024-07-25</td>
            <td>John Brown</td>
            <td>Product A</td>
            <td>3</td>
            <td>$50</td>
            <td>$150</td>
          </tr>
          <tr>
            <td>2024-07-27</td>
            <td>Ann Taylor</td>
            <td>Product A</td>
            <td>2</td>
            <td>$50</td>
            <td>$100</td>
          </tr>
          <tr>
            <td>2024-07-28</td>
            <td>Elizabeth Johnson</td>
            <td>Product C</td>
            <td>1</td>
            <td>$250</td>
            <td>$250</td>
          </tr>
          <tr>
            <td>2024-07-28</td>
            <td>Harry Brown</td>
            <td>Product B</td>
            <td>4</td>
            <td>$25</td>
            <td>$100</td>
          </tr>
          <tr>
            <td>2024-07-29</td>
            <td>Susan Clark</td>
            <td>Product D</td>
            <td>2</td>
            <td>$60</td>
            <td>$120</td>
          </tr>
          <tr>
            <td>2024-07-31</td>
            <td>Amanda Anderson</td>
            <td>Product B</td>
            <td>2</td>
            <td>$25</td>
            <td>$50</td>
          </tr>
          <tr>
            <td>2024-08-01</td>
            <td>Robert Smith</td>
            <td>Product C</td>
            <td>2</td>
            <td>$250</td>
            <td>$500</td>
          </tr>
          <tr>
            <td>2024-08-01</td>
            <td>Michael Miller</td>
            <td>Product A</td>
            <td>4</td>
            <td>$50</td>
            <td>$200</td>
          </tr>

          </tbody>
        </table>
      </div>

      <div class="footer">
        <p>&copy; 2024 Lady Amely. All rights reserved</p>
        <div class="social-icons">
          <a href="#facebook" title="Facebook">F</a>
          <a href="#instagram" title="Instagram">I</a>
          <a href="#linkedin" title="LinkedIn">L</a>
        </div>
      </div>

    </div>

  </div>
</template>

<script>

    export default {
      name: 'HelloWorld',
      props: {
        msg: String
      },
      data() {
        return {
          isSidebarOpen: false
        };
      },
      methods: {
        toggleSidebar() {
          this.isSidebarOpen = !this.isSidebarOpen;
        },
      }
    }




</script>


<style scoped>


html, body {
  margin: 0;
  padding: 0;
  height: 100%;
  overflow: hidden;
}

body {
  display: flex;
  flex-direction: row;
}

.sidebar {
  width: 250px;
  background-color: #ffffff;
  border-right: 2px solid #e0e0e0;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  transition: width 0.3s ease;
  z-index: 999;
}

.sidebar:hover {
  width: 300px;
}

.sidebar h1 {
  font-size: 24px;
  padding: 20px;
  margin: 0;
  color: #333;
}

.sidebar ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.sidebar ul li {
  border-bottom: 1px solid #e0e0e0;
}

.sidebar ul li a {
  display: block;
  padding: 15px 20px;
  text-decoration: none;
  color: #333;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.sidebar ul li a:hover i{
  background-color: #f0f0f0;
  color: rgba(27, 31, 37, 0.91);
}

.sidebar i {
  margin-right: 10px;
  color: #333;
  transition: color 0.3s ease;
}

.sidebar ul li a:hover i {
  background-color: rgba(240, 240, 240, 0);
  color: #75a7d8;
}

.content {
  flex: 1;
  padding: 20px;
  margin-left: 250px;
  transition: margin-left 0.3s ease;
}

.sidebar:hover + .content {
  margin-left: 300px;
}


.slide-enter-active, .slide-leave-active {
  transition: transform 0.7s ease;
}

.slide-enter {
  transform: translateX(-100%);
}

.slide-enter-to {
  transform: translateX(0%);
}

.slide-leave {
  transform: translateX(0%);
}

.slide-leave-to {
  transform: translateX(-100%);
}




.sidebar h3 {
  font-size: 22px;
  padding: 50px;
  margin: 0;
  margin-top: 50px;
  color: #333;
  font-family: 'Arial', sans-serif;
  font-weight: 600;
  border-bottom: 2px solid #e0e0e0;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  background-color: #f9f9f9;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.toggle-btn {
  position: fixed;
  top: 20px;
  left: 20px;
  z-index: 1000;
  background-color: #007bff;
  color: #ffffff;
  border: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.3s ease, box-shadow 0.3s ease;
}

.toggle-btn:hover {
  background-color: #0056b3;
  transform: scale(1.1);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
}

.toggle-btn i {
  font-size: 16px;
}

.sidebar-footer a {
  color: #2b2f3c;
  text-decoration: none;
  transition: color 0.3s ease;

}

.sidebar-footer p {
  color: #2b2f3c;
  text-decoration: none;
  transition: color 0.3s ease;
}

.sidebar-footer a:hover {
  text-decoration: underline;
}

.sidebar-footer .social-icons {
  margin-top: 10px;
}

.sidebar-footer .social-icons a {
  color: #333;
  margin: 0 10px;
  font-size: 20px;
  transition: color 0.3s ease;
}


.sidebar-footer .social-icons a:hover {
  color: #007bff;
}

.header {
  width: 100%;
  background-color: #ffffff;
  border-bottom: 2px solid #e0e0e0;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 20px;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
}

.header .logo {
  font-size: 20px;
  font-weight: bold;
  color: #333;
  text-decoration: none;
  margin-left: 50px;
}

.header .nav-links {
  display: flex;
  align-items: center;
}

.header .nav-links a {
  color: #333;
  text-decoration: none;
  padding: 0 15px;
  font-size: 16px;
  transition: color 0.3s ease;
}

.header .nav-links a:hover {
  color: #007bff;
}

.header .actions {
  display: flex;
  align-items: center;
}

.header .actions .action-btn {
  color: #333;
  font-size: 20px;
  margin-left: 15px;
  cursor: pointer;
  transition: color 0.3s ease;
}

.header .actions .action-btn:hover {
  color: #007bff;
}

h1 {
  font-size: 28px;
  margin-bottom: 10px;
  color: #333;
  font-family: 'Helvetica Neue','Arial', sans-serif;
  font-weight: 600;

}

.kpis {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

.kpi {
  background: linear-gradient(45deg, #23237a, #174180, #3283d1, rgb(117, 167, 216));
  padding: 20px;
  text-align: center;
  flex: 1;
  margin: 0 10px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06);
  margin-top: 20px;
}

.kpi-week {
  background: linear-gradient(45deg, #0380fb, #2e94cc, #2395b8, rgb(12, 239, 232));
  padding: 20px;
  text-align: center;
  flex: 1;
  margin: 0 10px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06);
  margin-top: 20px;
}

.kpi-month {
  background: linear-gradient(45deg, #0b63ba, #1c9ce1, #4ea4da, rgb(122, 188, 228));
  padding: 20px;
  text-align: center;
  flex: 1;
  margin: 0 10px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06);
  margin-top: 20px;
}

.kpi-total {
  background: linear-gradient(45deg, #23237a, #174180, #084075, rgb(12, 44, 76));
  padding: 20px;
  text-align: center;
  flex: 1;
  margin: 0 10px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06);
  margin-top: 20px;
}

.kpi-average {
  background: linear-gradient(45deg, #408eda, #387de4, #52b3ef, rgb(42, 208, 228));
  padding: 20px;
  text-align: center;
  flex: 1;
  margin: 0 10px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06);
  margin-top: 20px;
}

.kpi-new-customer {
  background: linear-gradient(45deg, #408eda, #5d97ed, #7dbbe1, rgb(117, 167, 216));
  padding: 20px;
  text-align: center;
  flex: 1;
  margin: 0 10px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06);
  margin-top: 20px;
}


.kpi h3 {
  margin-bottom: 10px;
  color: rgb(255, 255, 255);
  font-family: 'Helvetica Neue','Arial', sans-serif;
  font-weight: 600;

}

.kpi-new-customer h3 {
  margin-bottom: 10px;
  color: rgb(255, 255, 255);
  font-family: 'Helvetica Neue','Arial', sans-serif;
  font-weight: 600;

}

.kpi-week h3 {
  margin-bottom: 10px;
  color: rgb(255, 255, 255);
  font-family: 'Helvetica Neue','Arial', sans-serif;
  font-weight: 600;

}

.kpi-month h3 {
  margin-bottom: 10px;
  color: rgb(255, 255, 255);
  font-family: 'Helvetica Neue','Arial', sans-serif;
  font-weight: 600;

}

.kpi-total h3 {
  margin-bottom: 10px;
  color: rgb(255, 255, 255);
  font-family: 'Helvetica Neue','Arial', sans-serif;
  font-weight: 600;

}

.kpi-average h3 {
  margin-bottom: 10px;
  color: rgb(255, 255, 255);
  font-family: 'Helvetica Neue','Arial', sans-serif;
  font-weight: 600;

}

.transactions h3 {
  margin-bottom: 10px;
  color: #2c3e50;
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-weight: 700;
  text-transform: uppercase;
  margin-top: 40px;
}

.transactions table {
  width: 100%;
  border-collapse: collapse;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  overflow: hidden;
  margin-top: 5px;
}

.transactions table, .transactions th, .transactions td {
  border: 1px solid rgba(0, 0, 0, 0.1);
}

.transactions th, .transactions td {
  padding: 12px 15px;
  text-align: left;
  color: #34495e;
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-weight: 500;
}

.transactions th {
  background-color: #ecf0f1;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.transactions td {
  background-color: #ffffff;
  border-bottom: 1px solid #ecf0f1;
}
.transactions tr:nth-child(even) td {
  background-color: #f8f8f8;
}

.transactions tr:hover td {
  background-color: #dbe7f6;
}
p {
  font-size: 16px;
  margin-bottom: 20px;
  color: rgba(255, 255, 255, 0.48);
  font-family: 'Arial', sans-serif;
  font-weight: 600;
}


.alerts h3 {
  margin-bottom: 10px;
  color: #333;
  font-family: 'Arial', sans-serif;
  font-weight: 600;
}

.alerts p{
  font-size: 16px;
  margin-bottom: 20px;
  color: rgba(27, 31, 37, 0.91);
  font-family: 'Arial', sans-serif;
  font-weight: 600;


}

.footer {
  background-color: #2c3e50;
  color: #ecf0f1;
  font-family: 'Helvetica Neue', Arial, sans-serif;
  padding: 20px 0;
  text-align: center;
  border-top: 1px solid #34495e;
  margin-top: 20px;
}

.footer a {
  color: #ecf0f1;
  text-decoration: none;
  margin: 0 10px;
  transition: color 0.3s;
}

.footer a:hover {
  color: #0a6dcd;
}

.footer p {
  margin: 10px 0;
  font-size: 14px;
}

.footer .social-icons {
  margin-top: 10px;
}

.footer .social-icons a {
  margin: 0 5px;
  display: inline-block;
  width: 30px;
  height: 30px;
  background-color: #34495e;
  border-radius: 50%;
  line-height: 30px;
  font-size: 16px;
  transition: background-color 0.3s;
}

.footer .social-icons a:hover {
  background-color: #75a7d8;
}



</style>
