---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: 19c94fae0192766b87f430e6137fe8d3652325c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561028"
---
# <span data-ttu-id="2d5c8-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2d5c8-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="2d5c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="2d5c8-103">Удаляет службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d5c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d5c8-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d5c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="2d5c8-106">Командлет **Remove-AzureRmContainerService** Удаляет службу контейнеров из учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="2d5c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="2d5c8-108">Пример 1: Удаление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="2d5c8-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="2d5c8-109">Эта команда удаляет службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="2d5c8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d5c8-110">PARAMETERS</span></span>

### <span data-ttu-id="2d5c8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d5c8-111">-AsJob</span></span>
<span data-ttu-id="2d5c8-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2d5c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d5c8-113">-DefaultProfile</span></span>
<span data-ttu-id="2d5c8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d5c8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d5c8-115">-Force</span></span>
<span data-ttu-id="2d5c8-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d5c8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d5c8-117">-Name</span></span>
<span data-ttu-id="2d5c8-118">Указывает имя службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d5c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d5c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d5c8-120">Указывает группу ресурсов службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d5c8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d5c8-121">-Confirm</span></span>
<span data-ttu-id="2d5c8-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d5c8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d5c8-123">-WhatIf</span></span>
<span data-ttu-id="2d5c8-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d5c8-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d5c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d5c8-126">CommonParameters</span></span>
<span data-ttu-id="2d5c8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d5c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d5c8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d5c8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d5c8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d5c8-129">INPUTS</span></span>

### <span data-ttu-id="2d5c8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d5c8-130">System.String</span></span>

## <span data-ttu-id="2d5c8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d5c8-131">OUTPUTS</span></span>

### <span data-ttu-id="2d5c8-132">System. void</span><span class="sxs-lookup"><span data-stu-id="2d5c8-132">System.Void</span></span>

## <span data-ttu-id="2d5c8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d5c8-133">NOTES</span></span>

## <span data-ttu-id="2d5c8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d5c8-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d5c8-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2d5c8-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="2d5c8-136">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2d5c8-136">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="2d5c8-137">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2d5c8-137">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


