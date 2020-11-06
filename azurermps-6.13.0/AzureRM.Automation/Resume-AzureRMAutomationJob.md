---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 8e84f2f66703410b626769be8c2c2d5a57e531e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561172"
---
# <span data-ttu-id="d2be0-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d2be0-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="d2be0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2be0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2be0-103">Возобновление приостановленного задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d2be0-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2be0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2be0-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2be0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2be0-105">DESCRIPTION</span></span>
<span data-ttu-id="d2be0-106">Командлет **Resume-AzureRmAutomationJob** возобновляет приостановленное задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d2be0-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="d2be0-107">Укажите приостановленное задание.</span><span class="sxs-lookup"><span data-stu-id="d2be0-107">Specify the suspended job.</span></span>
<span data-ttu-id="d2be0-108">Чтобы приостановить задание, используйте командлет Suspend-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="d2be0-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="d2be0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2be0-109">EXAMPLES</span></span>

### <span data-ttu-id="d2be0-110">Пример 1: возобновление приостановленного задания</span><span class="sxs-lookup"><span data-stu-id="d2be0-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d2be0-111">Эта команда возобновляет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="d2be0-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="d2be0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2be0-112">PARAMETERS</span></span>

### <span data-ttu-id="d2be0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d2be0-113">-AutomationAccountName</span></span>
<span data-ttu-id="d2be0-114">Указывает имя учетной записи автоматизации, в которой этот командлет возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="d2be0-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2be0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2be0-115">-DefaultProfile</span></span>
<span data-ttu-id="d2be0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2be0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be0-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d2be0-117">-Id</span></span>
<span data-ttu-id="d2be0-118">Указывает идентификатор задания, возобновляемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="d2be0-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2be0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2be0-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2be0-120">Указывает имя группы ресурсов, для которой этот командлет возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="d2be0-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2be0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2be0-121">CommonParameters</span></span>
<span data-ttu-id="d2be0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2be0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2be0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2be0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2be0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2be0-124">INPUTS</span></span>

### <span data-ttu-id="d2be0-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d2be0-125">System.Guid</span></span>

### <span data-ttu-id="d2be0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d2be0-126">System.String</span></span>

## <span data-ttu-id="d2be0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2be0-127">OUTPUTS</span></span>

### <span data-ttu-id="d2be0-128">System. void</span><span class="sxs-lookup"><span data-stu-id="d2be0-128">System.Void</span></span>

## <span data-ttu-id="d2be0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2be0-129">NOTES</span></span>

## <span data-ttu-id="d2be0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2be0-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2be0-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d2be0-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="d2be0-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d2be0-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="d2be0-133">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d2be0-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="d2be0-134">Приостановить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d2be0-134">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


