---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 6d23fe3728b569cbb1a2aee498d560672ee75877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565669"
---
# <span data-ttu-id="521b8-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="521b8-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="521b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="521b8-102">SYNOPSIS</span></span>
<span data-ttu-id="521b8-103">Возобновление приостановленного задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="521b8-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="521b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="521b8-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="521b8-105">DESCRIPTION</span></span>
<span data-ttu-id="521b8-106">Командлет **Resume-AzureRmAutomationJob** возобновляет приостановленное задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="521b8-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="521b8-107">Укажите приостановленное задание.</span><span class="sxs-lookup"><span data-stu-id="521b8-107">Specify the suspended job.</span></span>

<span data-ttu-id="521b8-108">Чтобы приостановить задание, используйте командлет Suspend-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="521b8-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="521b8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="521b8-109">EXAMPLES</span></span>

### <span data-ttu-id="521b8-110">Пример 1: возобновление приостановленного задания</span><span class="sxs-lookup"><span data-stu-id="521b8-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="521b8-111">Эта команда возобновляет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="521b8-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="521b8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="521b8-112">PARAMETERS</span></span>

### <span data-ttu-id="521b8-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="521b8-113">-AutomationAccountName</span></span>
<span data-ttu-id="521b8-114">Указывает имя учетной записи автоматизации, в которой этот командлет возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="521b8-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="521b8-115">-ID</span><span class="sxs-lookup"><span data-stu-id="521b8-115">-Id</span></span>
<span data-ttu-id="521b8-116">Указывает идентификатор задания, возобновляемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="521b8-116">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="521b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="521b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="521b8-118">Указывает имя группы ресурсов, для которой этот командлет возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="521b8-118">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="521b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521b8-119">-DefaultProfile</span></span>
<span data-ttu-id="521b8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="521b8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="521b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521b8-121">CommonParameters</span></span>
<span data-ttu-id="521b8-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="521b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521b8-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521b8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521b8-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="521b8-124">INPUTS</span></span>

## <span data-ttu-id="521b8-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="521b8-125">OUTPUTS</span></span>

## <span data-ttu-id="521b8-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="521b8-126">NOTES</span></span>

## <span data-ttu-id="521b8-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="521b8-127">RELATED LINKS</span></span>

[<span data-ttu-id="521b8-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="521b8-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="521b8-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="521b8-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="521b8-130">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="521b8-130">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="521b8-131">Приостановить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="521b8-131">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


