---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: de8f9e05cbec17d6a92f3c4e567bd5dce96005ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566119"
---
# <span data-ttu-id="93d5c-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="93d5c-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="93d5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="93d5c-103">Удаление задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="93d5c-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93d5c-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="93d5c-106">Командлет **Remove-AzureRmSchedulerJob** удаляет задание планировщика Azure.</span><span class="sxs-lookup"><span data-stu-id="93d5c-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="93d5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93d5c-107">EXAMPLES</span></span>

## <span data-ttu-id="93d5c-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93d5c-108">PARAMETERS</span></span>

### <span data-ttu-id="93d5c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d5c-109">-DefaultProfile</span></span>
<span data-ttu-id="93d5c-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93d5c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d5c-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="93d5c-111">-JobCollectionName</span></span>
<span data-ttu-id="93d5c-112">Указывает имя коллекции заданий, которая содержит задание, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="93d5c-112">Specifies the name of a job collection that contains the job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93d5c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="93d5c-113">-JobName</span></span>
<span data-ttu-id="93d5c-114">Указывает имя задания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="93d5c-114">Specifies the name of a job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93d5c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93d5c-115">-PassThru</span></span>
<span data-ttu-id="93d5c-116">Указывает на то, что этот командлет возвращает значение успеха при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="93d5c-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="93d5c-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="93d5c-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d5c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d5c-118">-ResourceGroupName</span></span>
<span data-ttu-id="93d5c-119">Указывает группу ресурсов для задания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="93d5c-119">Specifies the resource group of the job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93d5c-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93d5c-120">-Confirm</span></span>
<span data-ttu-id="93d5c-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93d5c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d5c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d5c-122">-WhatIf</span></span>
<span data-ttu-id="93d5c-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93d5c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93d5c-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93d5c-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93d5c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d5c-125">CommonParameters</span></span>
<span data-ttu-id="93d5c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93d5c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d5c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d5c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d5c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93d5c-128">INPUTS</span></span>

### <span data-ttu-id="93d5c-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="93d5c-129">None</span></span>
<span data-ttu-id="93d5c-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="93d5c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93d5c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93d5c-131">OUTPUTS</span></span>

## <span data-ttu-id="93d5c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="93d5c-132">NOTES</span></span>

## <span data-ttu-id="93d5c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93d5c-133">RELATED LINKS</span></span>

[<span data-ttu-id="93d5c-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="93d5c-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


