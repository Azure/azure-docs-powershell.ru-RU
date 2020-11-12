---
title: Запуск командлетов Azure PowerShell в заданиях PowerShell
description: Сведения о параллельном запуске командлетов Azure PowerShell или запуске в качестве фоновых задач, используя -AsJob и Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b76e310e1677e539927ebc4746df67c1d1accc16
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407720"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="64cc4-103">Запуск командлетов Azure PowerShell в заданиях PowerShell</span><span class="sxs-lookup"><span data-stu-id="64cc4-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="64cc4-104">Azure PowerShell зависит от подключения к облаку Azure и ожидания ответов, поэтому большинство этих командлетов блокируют сеанс PowerShell до получения ответа из облака.</span><span class="sxs-lookup"><span data-stu-id="64cc4-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="64cc4-105">Задания Powershell позволяют запускать командлеты в фоновом режиме или одновременно выполнять несколько задач в Azure из одного сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64cc4-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="64cc4-106">В этой статье приводится краткий обзор запуска командлетов Azure PowerShell в качестве заданий PowerShell, а также проверки их выполнения.</span><span class="sxs-lookup"><span data-stu-id="64cc4-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="64cc4-107">Для запуска команд в Azure PowerShell необходимо использовать контексты Azure PowerShell, которые подробно описаны в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="64cc4-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="64cc4-108">Дополнительные сведения о заданиях PowerShell, см. раздел [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs) (Сведения о заданиях PowerShell).</span><span class="sxs-lookup"><span data-stu-id="64cc4-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="64cc4-109">Контексты Azure с заданиями PowerShell</span><span class="sxs-lookup"><span data-stu-id="64cc4-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="64cc4-110">Задания PowerShell выполняются как отдельные процессы без подключенного сеанса PowerShell, поэтому им необходимо предоставить ваши учетные данные Azure.</span><span class="sxs-lookup"><span data-stu-id="64cc4-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="64cc4-111">Учетные данные передаются как объекты контекста Azure одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="64cc4-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="64cc4-112">Автоматическое сохранение контекста.</span><span class="sxs-lookup"><span data-stu-id="64cc4-112">Automatic context persistence.</span></span> <span data-ttu-id="64cc4-113">Сохраняемость контекста включена по умолчанию и сохраняет данные для входа в нескольких сеансах.</span><span class="sxs-lookup"><span data-stu-id="64cc4-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="64cc4-114">При включенной сохраняемости контекста текущий контекст Azure передается новому процессу:</span><span class="sxs-lookup"><span data-stu-id="64cc4-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="64cc4-115">Используйте параметр `-AzContext` с любыми командлетами Azure PowerShell, чтобы предоставить объект контекста Azure:</span><span class="sxs-lookup"><span data-stu-id="64cc4-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="64cc4-116">Если сохраняемость контекста отключена, аргумент `-AzContext` является обязательным.</span><span class="sxs-lookup"><span data-stu-id="64cc4-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="64cc4-117">Используйте переключатель `-AsJob`, предоставляемый некоторыми командлетами Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64cc4-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="64cc4-118">Этот переключатель автоматически запускает командлет как задание PowerShell, используя текущий активный контекст Azure:</span><span class="sxs-lookup"><span data-stu-id="64cc4-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="64cc4-119">Чтобы узнать, поддерживает ли командлет `-AsJob`, проверьте его справочную документацию.</span><span class="sxs-lookup"><span data-stu-id="64cc4-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="64cc4-120">Переключатель `-AsJob` не требует включения автосохранения контекста.</span><span class="sxs-lookup"><span data-stu-id="64cc4-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="64cc4-121">Состояние запущенного задания можно проверить с помощью командлета [Get-Job](/powershell/module/microsoft.powershell.core/get-job).</span><span class="sxs-lookup"><span data-stu-id="64cc4-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="64cc4-122">Чтобы получить выходные данные задания, используйте командлет [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).</span><span class="sxs-lookup"><span data-stu-id="64cc4-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="64cc4-123">Чтобы удаленно проверять ход выполнения операции в Azure, используйте командлеты `Get-`, связанные с типом ресурса, изменяемого заданием:</span><span class="sxs-lookup"><span data-stu-id="64cc4-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="64cc4-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="64cc4-124">See Also</span></span>

* [<span data-ttu-id="64cc4-125">Контексты Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="64cc4-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* <span data-ttu-id="64cc4-126">[About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs) (Сведения о заданиях PowerShell)</span><span class="sxs-lookup"><span data-stu-id="64cc4-126">[About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)</span></span>
* [<span data-ttu-id="64cc4-127">Справочные материалы по Get-Job</span><span class="sxs-lookup"><span data-stu-id="64cc4-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="64cc4-128">Справочные материалы по Receive-Job</span><span class="sxs-lookup"><span data-stu-id="64cc4-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
