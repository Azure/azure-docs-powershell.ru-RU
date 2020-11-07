---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913064"
---
# <span data-ttu-id="004e0-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="004e0-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="004e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="004e0-102">SYNOPSIS</span></span>
<span data-ttu-id="004e0-103">Удаляет службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="004e0-103">Removes a container service.</span></span>

## <span data-ttu-id="004e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="004e0-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="004e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="004e0-105">DESCRIPTION</span></span>
<span data-ttu-id="004e0-106">Командлет **Remove-AzContainerService** Удаляет службу контейнеров из учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="004e0-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="004e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="004e0-107">EXAMPLES</span></span>

### <span data-ttu-id="004e0-108">Пример 1: Удаление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="004e0-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="004e0-109">Эта команда удаляет службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="004e0-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="004e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="004e0-110">PARAMETERS</span></span>

### <span data-ttu-id="004e0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="004e0-111">-AsJob</span></span>
<span data-ttu-id="004e0-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="004e0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="004e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004e0-113">-DefaultProfile</span></span>
<span data-ttu-id="004e0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="004e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="004e0-115">-Force</span></span>
<span data-ttu-id="004e0-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="004e0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="004e0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="004e0-117">-Name</span></span>
<span data-ttu-id="004e0-118">Указывает имя службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="004e0-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="004e0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004e0-119">-ResourceGroupName</span></span>
<span data-ttu-id="004e0-120">Указывает группу ресурсов службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="004e0-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="004e0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="004e0-121">-Confirm</span></span>
<span data-ttu-id="004e0-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="004e0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004e0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004e0-123">-WhatIf</span></span>
<span data-ttu-id="004e0-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="004e0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="004e0-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="004e0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004e0-126">CommonParameters</span></span>
<span data-ttu-id="004e0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="004e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004e0-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="004e0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004e0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="004e0-129">INPUTS</span></span>

### <span data-ttu-id="004e0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="004e0-130">System.String</span></span>

## <span data-ttu-id="004e0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="004e0-131">OUTPUTS</span></span>

### <span data-ttu-id="004e0-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="004e0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="004e0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="004e0-133">NOTES</span></span>

## <span data-ttu-id="004e0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="004e0-134">RELATED LINKS</span></span>

[<span data-ttu-id="004e0-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="004e0-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="004e0-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="004e0-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="004e0-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="004e0-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


