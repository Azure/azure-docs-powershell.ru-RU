---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/enable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 832b7659da0b71d804ddc1a8f19703b85fc8500b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733997"
---
# <span data-ttu-id="a4f1f-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a4f1f-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="a4f1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f1f-103">Включает коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4f1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4f1f-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f1f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f1f-106">Командлет **Enable-AzureRmSchedulerJobCollection** включает коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="a4f1f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4f1f-107">EXAMPLES</span></span>

## <span data-ttu-id="a4f1f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4f1f-108">PARAMETERS</span></span>

### <span data-ttu-id="a4f1f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f1f-109">-DefaultProfile</span></span>
<span data-ttu-id="a4f1f-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4f1f-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a4f1f-111">-JobCollectionName</span></span>
<span data-ttu-id="a4f1f-112">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="a4f1f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4f1f-113">-PassThru</span></span>
<span data-ttu-id="a4f1f-114">Указывает на то, что этот командлет возвращает значение успеха при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="a4f1f-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4f1f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f1f-116">-ResourceGroupName</span></span>
<span data-ttu-id="a4f1f-117">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="a4f1f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4f1f-118">-Confirm</span></span>
<span data-ttu-id="a4f1f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f1f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f1f-120">-WhatIf</span></span>
<span data-ttu-id="a4f1f-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f1f-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f1f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f1f-123">CommonParameters</span></span>
<span data-ttu-id="a4f1f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f1f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f1f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f1f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4f1f-126">INPUTS</span></span>

### <span data-ttu-id="a4f1f-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4f1f-127">None</span></span>
<span data-ttu-id="a4f1f-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a4f1f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4f1f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4f1f-129">OUTPUTS</span></span>

## <span data-ttu-id="a4f1f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4f1f-130">NOTES</span></span>

## <span data-ttu-id="a4f1f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4f1f-131">RELATED LINKS</span></span>

[<span data-ttu-id="a4f1f-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a4f1f-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a4f1f-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a4f1f-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a4f1f-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a4f1f-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a4f1f-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a4f1f-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a4f1f-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a4f1f-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


