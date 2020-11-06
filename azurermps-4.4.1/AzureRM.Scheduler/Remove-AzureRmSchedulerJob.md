---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 582953886b8ea39e04dee122c85d70884dabcf11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565156"
---
# <span data-ttu-id="d7e10-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d7e10-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="d7e10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7e10-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e10-103">Удаление задания планировщика.</span><span class="sxs-lookup"><span data-stu-id="d7e10-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7e10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7e10-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7e10-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7e10-105">DESCRIPTION</span></span>
<span data-ttu-id="d7e10-106">Командлет **Remove-AzureRmSchedulerJob** удаляет задание планировщика Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e10-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="d7e10-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7e10-107">EXAMPLES</span></span>

## <span data-ttu-id="d7e10-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7e10-108">PARAMETERS</span></span>

### <span data-ttu-id="d7e10-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d7e10-109">-JobCollectionName</span></span>
<span data-ttu-id="d7e10-110">Указывает имя коллекции заданий, которая содержит задание, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d7e10-110">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="d7e10-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="d7e10-111">-JobName</span></span>
<span data-ttu-id="d7e10-112">Указывает имя задания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d7e10-112">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="d7e10-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7e10-113">-PassThru</span></span>
<span data-ttu-id="d7e10-114">Указывает на то, что этот командлет возвращает значение успеха при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="d7e10-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="d7e10-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d7e10-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e10-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e10-116">-ResourceGroupName</span></span>
<span data-ttu-id="d7e10-117">Указывает группу ресурсов для задания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d7e10-117">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="d7e10-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7e10-118">-Confirm</span></span>
<span data-ttu-id="d7e10-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7e10-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e10-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e10-120">-WhatIf</span></span>
<span data-ttu-id="d7e10-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7e10-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7e10-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7e10-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e10-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e10-123">-DefaultProfile</span></span>
<span data-ttu-id="d7e10-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e10-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7e10-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e10-125">CommonParameters</span></span>
<span data-ttu-id="d7e10-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7e10-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e10-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e10-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e10-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7e10-128">INPUTS</span></span>

## <span data-ttu-id="d7e10-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7e10-129">OUTPUTS</span></span>

## <span data-ttu-id="d7e10-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7e10-130">NOTES</span></span>

## <span data-ttu-id="d7e10-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7e10-131">RELATED LINKS</span></span>

[<span data-ttu-id="d7e10-132">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d7e10-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


