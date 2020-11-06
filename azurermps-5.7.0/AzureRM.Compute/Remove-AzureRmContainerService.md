---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559172"
---
# <span data-ttu-id="fca86-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fca86-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="fca86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fca86-102">SYNOPSIS</span></span>
<span data-ttu-id="fca86-103">Удаляет службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="fca86-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fca86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fca86-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fca86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca86-105">DESCRIPTION</span></span>
<span data-ttu-id="fca86-106">Командлет **Remove-AzureRmContainerService** Удаляет службу контейнеров из учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="fca86-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="fca86-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fca86-107">EXAMPLES</span></span>

### <span data-ttu-id="fca86-108">Пример 1: Удаление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="fca86-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="fca86-109">Эта команда удаляет службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="fca86-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="fca86-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fca86-110">PARAMETERS</span></span>

### <span data-ttu-id="fca86-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fca86-111">-Force</span></span>
<span data-ttu-id="fca86-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fca86-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca86-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fca86-113">-Name</span></span>
<span data-ttu-id="fca86-114">Указывает имя службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fca86-114">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fca86-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca86-115">-ResourceGroupName</span></span>
<span data-ttu-id="fca86-116">Указывает группу ресурсов службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fca86-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fca86-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fca86-117">-Confirm</span></span>
<span data-ttu-id="fca86-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fca86-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="fca86-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca86-119">-WhatIf</span></span>
<span data-ttu-id="fca86-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fca86-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fca86-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fca86-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="fca86-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca86-122">CommonParameters</span></span>
<span data-ttu-id="fca86-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fca86-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca86-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca86-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca86-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fca86-125">INPUTS</span></span>

### <span data-ttu-id="fca86-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="fca86-126">None</span></span>
<span data-ttu-id="fca86-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fca86-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fca86-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca86-128">OUTPUTS</span></span>

## <span data-ttu-id="fca86-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fca86-129">NOTES</span></span>

## <span data-ttu-id="fca86-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fca86-130">RELATED LINKS</span></span>

[<span data-ttu-id="fca86-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fca86-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="fca86-132">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fca86-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="fca86-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fca86-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


