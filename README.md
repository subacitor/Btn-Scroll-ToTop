# Btn-Scroll-ToTop
.html
================================================
  <button type="button" class="scroll-to-top btn-position btnstyle" onclick="goToTop();"><i
    class="fa-solid fa-angle-up"></i></button>
================================================

.css
================================================
scroll-to-top {
    position: relative;
}
.btn-position {
    position: fixed;
    bottom: 30px;
    right: 25px;
    z-index: 20;

}
.btnstyle {
    background-color: rgb(95, 174, 179);
    border: none;
    border-radius: 7px;
    font-weight: lighter;
    height: 40px;
    width: 40px;
    color: #fff;
    cursor: pointer;
    /* transition: all 0.5s ease-in-out; */
    font-size: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0;
    z-index: 99;
}
.btnstyle {
    transition-timing-function: ease;
}

.btnstyle.active {
    opacity: 1;
}

================================================
.jss
================================================
 const nav = document.querySelector("nav");
    const btnstyle = document.querySelector(".btnstyle");
    btnstyle.addEventListener("click", function () {
      window.scrollTo({ top: 0, left: 0, behavior: "smooth" });
    });
    window.addEventListener("scroll", () => {
      if (window.pageYOffset > 90) {
        btnstyle.classList.add("active");
      } else {
        btnstyle.classList.remove("active");
      }
    });

================================================


