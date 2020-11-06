---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 7eec69a441efbf1a4d9f73e85a0385c24a012e34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567518"
---
# <span data-ttu-id="2237e-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="2237e-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="2237e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2237e-102">SYNOPSIS</span></span>
<span data-ttu-id="2237e-103">Получение журнала заданий.</span><span class="sxs-lookup"><span data-stu-id="2237e-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2237e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2237e-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2237e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2237e-105">DESCRIPTION</span></span>
<span data-ttu-id="2237e-106">Командлет **Get-AzureRmSchedulerJobHistory** получает историю для задания планировщика Azure.</span><span class="sxs-lookup"><span data-stu-id="2237e-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="2237e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2237e-107">EXAMPLES</span></span>

## <span data-ttu-id="2237e-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2237e-108">PARAMETERS</span></span>

### <span data-ttu-id="2237e-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2237e-109">-JobCollectionName</span></span>
<span data-ttu-id="2237e-110">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="2237e-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2237e-111">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="2237e-111">-JobExecutionStatus</span></span>
<span data-ttu-id="2237e-112">Указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="2237e-112">Specifies the status of a job.</span></span>
<span data-ttu-id="2237e-113">Этот командлет получает историю, которая соответствует указанному вами статусу.</span><span class="sxs-lookup"><span data-stu-id="2237e-113">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="2237e-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2237e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2237e-115">Completed</span><span class="sxs-lookup"><span data-stu-id="2237e-115">Completed</span></span> 
- <span data-ttu-id="2237e-116">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="2237e-116">Failed</span></span> 
- <span data-ttu-id="2237e-117">Отложена</span><span class="sxs-lookup"><span data-stu-id="2237e-117">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2237e-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="2237e-118">-JobName</span></span>
<span data-ttu-id="2237e-119">Указывает имя задания, для которого этот командлет получает историю.</span><span class="sxs-lookup"><span data-stu-id="2237e-119">Specifies the name of a job for which this cmdlet gets history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2237e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2237e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2237e-121">Указывает группу ресурсов, к которой относится задание.</span><span class="sxs-lookup"><span data-stu-id="2237e-121">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2237e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2237e-122">-DefaultProfile</span></span>
<span data-ttu-id="2237e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2237e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2237e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2237e-124">CommonParameters</span></span>
<span data-ttu-id="2237e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2237e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2237e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2237e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2237e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2237e-127">INPUTS</span></span>

## <span data-ttu-id="2237e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2237e-128">OUTPUTS</span></span>

### <span data-ttu-id="2237e-129">Microsoft. Azure. Commands. Scheduler. Models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="2237e-129">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="2237e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2237e-130">NOTES</span></span>

## <span data-ttu-id="2237e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2237e-131">RELATED LINKS</span></span>

[<span data-ttu-id="2237e-132">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="2237e-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


