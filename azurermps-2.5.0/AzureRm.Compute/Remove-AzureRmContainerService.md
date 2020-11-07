---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914554"
---
# <span data-ttu-id="50fba-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="50fba-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="50fba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50fba-102">SYNOPSIS</span></span>
<span data-ttu-id="50fba-103">Удаляет службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="50fba-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50fba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50fba-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50fba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50fba-105">DESCRIPTION</span></span>
<span data-ttu-id="50fba-106">Командлет **Remove-AzureRmContainerService** Удаляет службу контейнеров из учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="50fba-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="50fba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50fba-107">EXAMPLES</span></span>

### <span data-ttu-id="50fba-108">Пример 1: Удаление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="50fba-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="50fba-109">Эта команда удаляет службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="50fba-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="50fba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50fba-110">PARAMETERS</span></span>

### <span data-ttu-id="50fba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50fba-111">-AsJob</span></span>
<span data-ttu-id="50fba-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="50fba-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="50fba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fba-113">-DefaultProfile</span></span>
<span data-ttu-id="50fba-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50fba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50fba-115">-Force</span><span class="sxs-lookup"><span data-stu-id="50fba-115">-Force</span></span>
<span data-ttu-id="50fba-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="50fba-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50fba-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50fba-117">-Name</span></span>
<span data-ttu-id="50fba-118">Указывает имя службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="50fba-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50fba-119">-ResourceGroupName</span></span>
<span data-ttu-id="50fba-120">Указывает группу ресурсов службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="50fba-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fba-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50fba-121">-Confirm</span></span>
<span data-ttu-id="50fba-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50fba-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="50fba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fba-123">-WhatIf</span></span>
<span data-ttu-id="50fba-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50fba-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50fba-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50fba-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="50fba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fba-126">CommonParameters</span></span>
<span data-ttu-id="50fba-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50fba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fba-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50fba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fba-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50fba-129">INPUTS</span></span>

### <span data-ttu-id="50fba-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="50fba-130">None</span></span>
<span data-ttu-id="50fba-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="50fba-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50fba-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50fba-132">OUTPUTS</span></span>

### <span data-ttu-id="50fba-133">System. void</span><span class="sxs-lookup"><span data-stu-id="50fba-133">System.Void</span></span>

## <span data-ttu-id="50fba-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="50fba-134">NOTES</span></span>

## <span data-ttu-id="50fba-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50fba-135">RELATED LINKS</span></span>

[<span data-ttu-id="50fba-136">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="50fba-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="50fba-137">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="50fba-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="50fba-138">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="50fba-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


