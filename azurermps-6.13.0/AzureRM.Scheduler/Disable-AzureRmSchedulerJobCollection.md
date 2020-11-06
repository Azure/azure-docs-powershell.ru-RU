---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 9673c236886feb801d6e4078bfccbf82e2339811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562660"
---
# <span data-ttu-id="3fdd7-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fdd7-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="3fdd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fdd7-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdd7-103">Отключение коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fdd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fdd7-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fdd7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fdd7-105">DESCRIPTION</span></span>
<span data-ttu-id="3fdd7-106">Командлет **Disable-AzureRmSchedulerJobCollection** отключает коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="3fdd7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fdd7-107">EXAMPLES</span></span>

## <span data-ttu-id="3fdd7-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fdd7-108">PARAMETERS</span></span>

### <span data-ttu-id="3fdd7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdd7-109">-DefaultProfile</span></span>
<span data-ttu-id="3fdd7-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fdd7-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3fdd7-111">-JobCollectionName</span></span>
<span data-ttu-id="3fdd7-112">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="3fdd7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fdd7-113">-PassThru</span></span>
<span data-ttu-id="3fdd7-114">Указывает на то, что этот командлет возвращает значение успеха при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="3fdd7-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fdd7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdd7-116">-ResourceGroupName</span></span>
<span data-ttu-id="3fdd7-117">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="3fdd7-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fdd7-118">-Confirm</span></span>
<span data-ttu-id="3fdd7-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fdd7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fdd7-120">-WhatIf</span></span>
<span data-ttu-id="3fdd7-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fdd7-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fdd7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdd7-123">CommonParameters</span></span>
<span data-ttu-id="3fdd7-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fdd7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdd7-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fdd7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdd7-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fdd7-126">INPUTS</span></span>

### <span data-ttu-id="3fdd7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3fdd7-127">System.String</span></span>

## <span data-ttu-id="3fdd7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fdd7-128">OUTPUTS</span></span>

### <span data-ttu-id="3fdd7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3fdd7-129">System.String</span></span>

## <span data-ttu-id="3fdd7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fdd7-130">NOTES</span></span>

## <span data-ttu-id="3fdd7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fdd7-131">RELATED LINKS</span></span>

[<span data-ttu-id="3fdd7-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fdd7-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3fdd7-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fdd7-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3fdd7-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fdd7-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3fdd7-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fdd7-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3fdd7-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3fdd7-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


