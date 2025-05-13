# ecen5033-homework-4-solved
**TO GET THIS SOLUTION VISIT:** [ECEN5033 Homework 4 Solved](https://www.ankitcodinghub.com/product/ecen5033-homework-4-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92251&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECEN5033 Homework 4 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
In HW2, you created two docker containers – a client which continuously makes requests to a server which will respond with some message. In HW3 you enabled upgrading the server (with a new message). In HW4, you’ll expand this to run in Kubernetes, with some modifications – namely, the server returns it’s own hostname and some hard coded message.

Note: njsapp that I provided includes the hostname, so you just need to extend that a bit.

PART 1:

Server must: 1) be able to scale out, 2) tolerate failure.

Use ReplicationController and a Service.

Server instances must run on machine2 (need nodeSelector)

Client must run on machine3 (need nodeSelector)

&nbsp;

PART 2:

Now, support upgrades. Without bringing down the server.

Easiest way will be create a deployment (which will launch new Pods), then delete the Replication controller. You could also delete the Replication controller without deleting the Pods (recall kubectl delete rc &lt;name&gt; –cascade=false won’t delete the pods), then launch a Deployment.

https://upendra-kumarage.medium.com/kubernetes-replicationcontrollers-deployments-and-update-existing-replicationcontroller-to-3b0ecf0bf349

Then, demonstrate an upgrade by changing the message of the server.

HAND IN:

1) Dockerfiles (even if they were unchanged from what was handed out),

2) Build scripts (builds container and pushes to registry),

3) yaml files,

4) README with exact sequence of commands to run to verify all of the above (including killing some pods, scaling out, changing to a deployment, and then upgrading the server).

Assumptions:

* I (and your peer) have Kubernetes installed with 3 VMs (machine1-3), I (and your peer) will have a Registry running at 192.168.33.10:5000

* Each Student will put all of their files in a unique directory. &lt;firstname&gt;_HW4

/home/vagrant/eric_HW4

/home/vagrant/karl_HW4

* Image names and resource names should all start with student’s first name.

e.g., eric-njsapp, eric-njsapp-svc, etc.

&nbsp;
