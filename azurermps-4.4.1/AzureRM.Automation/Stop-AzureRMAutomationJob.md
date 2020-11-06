---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: db7e76a21f635429be598ca9f40899ece3fa0406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568341"
---
# <span data-ttu-id="05789-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05789-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="05789-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05789-102">SYNOPSIS</span></span>
<span data-ttu-id="05789-103">Остановка задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="05789-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05789-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05789-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05789-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05789-105">DESCRIPTION</span></span>
<span data-ttu-id="05789-106">Командлет **Stop-AzureRmAutomationJob** останавливает задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="05789-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="05789-107">Укажите выполнение задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="05789-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="05789-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05789-108">EXAMPLES</span></span>

### <span data-ttu-id="05789-109">Пример 1: Остановка задания</span><span class="sxs-lookup"><span data-stu-id="05789-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05789-110">Эта команда останавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="05789-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="05789-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05789-111">PARAMETERS</span></span>

### <span data-ttu-id="05789-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05789-112">-AutomationAccountName</span></span>
<span data-ttu-id="05789-113">Указывает имя учетной записи автоматизации, в которой этот командлет останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="05789-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="05789-114">-ID</span><span class="sxs-lookup"><span data-stu-id="05789-114">-Id</span></span>
<span data-ttu-id="05789-115">Указывает идентификатор задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="05789-115">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="05789-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05789-116">-ResourceGroupName</span></span>
<span data-ttu-id="05789-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05789-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="05789-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05789-118">-DefaultProfile</span></span>
<span data-ttu-id="05789-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05789-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05789-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05789-120">CommonParameters</span></span>
<span data-ttu-id="05789-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05789-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05789-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05789-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05789-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05789-123">INPUTS</span></span>

## <span data-ttu-id="05789-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05789-124">OUTPUTS</span></span>

## <span data-ttu-id="05789-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="05789-125">NOTES</span></span>

## <span data-ttu-id="05789-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05789-126">RELATED LINKS</span></span>

[<span data-ttu-id="05789-127">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05789-127">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="05789-128">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="05789-128">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="05789-129">Возобновить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05789-129">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="05789-130">Приостановить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05789-130">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


