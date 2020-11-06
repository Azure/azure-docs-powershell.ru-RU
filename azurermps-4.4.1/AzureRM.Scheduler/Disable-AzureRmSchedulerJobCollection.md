---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 3078bddfe82fa1280e7f3288f86c572c44a99148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565159"
---
# <span data-ttu-id="d7def-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7def-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d7def-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7def-102">SYNOPSIS</span></span>
<span data-ttu-id="d7def-103">Отключение коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="d7def-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7def-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7def-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7def-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7def-105">DESCRIPTION</span></span>
<span data-ttu-id="d7def-106">Командлет **Disable-AzureRmSchedulerJobCollection** отключает коллекцию заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="d7def-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d7def-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7def-107">EXAMPLES</span></span>

## <span data-ttu-id="d7def-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7def-108">PARAMETERS</span></span>

### <span data-ttu-id="d7def-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d7def-109">-JobCollectionName</span></span>
<span data-ttu-id="d7def-110">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="d7def-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="d7def-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7def-111">-PassThru</span></span>
<span data-ttu-id="d7def-112">Указывает на то, что этот командлет возвращает значение успеха при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="d7def-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="d7def-113">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d7def-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7def-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7def-114">-ResourceGroupName</span></span>
<span data-ttu-id="d7def-115">Указывает группу ресурсов для коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="d7def-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="d7def-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7def-116">-Confirm</span></span>
<span data-ttu-id="d7def-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7def-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7def-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7def-118">-WhatIf</span></span>
<span data-ttu-id="d7def-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7def-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7def-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7def-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7def-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7def-121">-DefaultProfile</span></span>
<span data-ttu-id="d7def-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7def-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7def-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7def-123">CommonParameters</span></span>
<span data-ttu-id="d7def-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7def-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7def-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7def-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7def-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7def-126">INPUTS</span></span>

## <span data-ttu-id="d7def-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7def-127">OUTPUTS</span></span>

## <span data-ttu-id="d7def-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7def-128">NOTES</span></span>

## <span data-ttu-id="d7def-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7def-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7def-130">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7def-130">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7def-131">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7def-131">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7def-132">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7def-132">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7def-133">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7def-133">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7def-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7def-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


