---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b1caa041f92312d3d122e758a9e63bc7299887b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565155"
---
# <span data-ttu-id="91f4f-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="91f4f-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="91f4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="91f4f-103">Удаляет коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="91f4f-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91f4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91f4f-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91f4f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="91f4f-106">Командлет **Remove-AzureRmSchedulerJobCollection** удаляет коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="91f4f-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="91f4f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91f4f-107">EXAMPLES</span></span>

## <span data-ttu-id="91f4f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91f4f-108">PARAMETERS</span></span>

### <span data-ttu-id="91f4f-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="91f4f-109">-JobCollectionName</span></span>
<span data-ttu-id="91f4f-110">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="91f4f-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="91f4f-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91f4f-111">-PassThru</span></span>
<span data-ttu-id="91f4f-112">Указывает на то, что этот командлет возвращает значение успеха при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="91f4f-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="91f4f-113">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="91f4f-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91f4f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f4f-114">-ResourceGroupName</span></span>
<span data-ttu-id="91f4f-115">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="91f4f-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="91f4f-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91f4f-116">-Confirm</span></span>
<span data-ttu-id="91f4f-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="91f4f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f4f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f4f-118">-WhatIf</span></span>
<span data-ttu-id="91f4f-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="91f4f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f4f-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="91f4f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f4f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f4f-121">-DefaultProfile</span></span>
<span data-ttu-id="91f4f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91f4f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91f4f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f4f-123">CommonParameters</span></span>
<span data-ttu-id="91f4f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91f4f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f4f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f4f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f4f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91f4f-126">INPUTS</span></span>

## <span data-ttu-id="91f4f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91f4f-127">OUTPUTS</span></span>

## <span data-ttu-id="91f4f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="91f4f-128">NOTES</span></span>

## <span data-ttu-id="91f4f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91f4f-129">RELATED LINKS</span></span>

[<span data-ttu-id="91f4f-130">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="91f4f-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="91f4f-131">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="91f4f-131">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="91f4f-132">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="91f4f-132">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="91f4f-133">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="91f4f-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="91f4f-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="91f4f-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


