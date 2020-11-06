---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 1a977578b278c51d8e66b0f502ba12fbac39e810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560660"
---
# <span data-ttu-id="b4169-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b4169-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="b4169-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4169-102">SYNOPSIS</span></span>
<span data-ttu-id="b4169-103">Удаляет коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="b4169-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4169-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4169-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4169-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4169-105">DESCRIPTION</span></span>
<span data-ttu-id="b4169-106">Командлет **Remove-AzureRmSchedulerJobCollection** удаляет коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="b4169-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="b4169-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4169-107">EXAMPLES</span></span>

## <span data-ttu-id="b4169-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4169-108">PARAMETERS</span></span>

### <span data-ttu-id="b4169-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4169-109">-DefaultProfile</span></span>
<span data-ttu-id="b4169-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4169-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4169-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b4169-111">-JobCollectionName</span></span>
<span data-ttu-id="b4169-112">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="b4169-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="b4169-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4169-113">-PassThru</span></span>
<span data-ttu-id="b4169-114">Указывает на то, что этот командлет возвращает значение успеха при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="b4169-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="b4169-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b4169-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4169-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4169-116">-ResourceGroupName</span></span>
<span data-ttu-id="b4169-117">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="b4169-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="b4169-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4169-118">-Confirm</span></span>
<span data-ttu-id="b4169-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4169-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4169-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4169-120">-WhatIf</span></span>
<span data-ttu-id="b4169-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4169-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4169-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4169-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4169-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4169-123">CommonParameters</span></span>
<span data-ttu-id="b4169-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4169-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4169-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4169-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4169-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4169-126">INPUTS</span></span>

### <span data-ttu-id="b4169-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b4169-127">System.String</span></span>

## <span data-ttu-id="b4169-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4169-128">OUTPUTS</span></span>

### <span data-ttu-id="b4169-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b4169-129">System.String</span></span>

## <span data-ttu-id="b4169-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4169-130">NOTES</span></span>

## <span data-ttu-id="b4169-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4169-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4169-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b4169-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b4169-133">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b4169-133">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b4169-134">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b4169-134">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b4169-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b4169-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b4169-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b4169-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


