---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557464"
---
# <span data-ttu-id="73040-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="73040-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="73040-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73040-102">SYNOPSIS</span></span>
<span data-ttu-id="73040-103">Запускает обновление экземпляра VMSS вручную.</span><span class="sxs-lookup"><span data-stu-id="73040-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73040-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73040-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73040-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73040-105">DESCRIPTION</span></span>
<span data-ttu-id="73040-106">Командлет Update-AzureRmVmssInstance запускает ручное обновление указанного экземпляра установленного набора масштаба виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="73040-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="73040-107">Этот параметр используется, если для политики обновления в VMSS масштабе задано значение "вручную".</span><span class="sxs-lookup"><span data-stu-id="73040-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="73040-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73040-108">EXAMPLES</span></span>

### <span data-ttu-id="73040-109">Пример 1: Начало обновления экземпляра VMSS</span><span class="sxs-lookup"><span data-stu-id="73040-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="73040-110">Эта команда запускает обновление VMSS с именем VMScaleSet001, которое содержит идентификатор экземпляра 0.</span><span class="sxs-lookup"><span data-stu-id="73040-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="73040-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73040-111">PARAMETERS</span></span>

### <span data-ttu-id="73040-112">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="73040-112">-InstanceId</span></span>
<span data-ttu-id="73040-113">Задает в качестве строкового массива идентификатор или идентификаторы экземпляра для обновления.</span><span class="sxs-lookup"><span data-stu-id="73040-113">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73040-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73040-114">-ResourceGroupName</span></span>
<span data-ttu-id="73040-115">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="73040-115">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="73040-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="73040-116">-VMScaleSetName</span></span>
<span data-ttu-id="73040-117">Указывает имя экземпляра VMSS, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="73040-117">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73040-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73040-118">-Confirm</span></span>
<span data-ttu-id="73040-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73040-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73040-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73040-120">-WhatIf</span></span>
<span data-ttu-id="73040-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73040-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="73040-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73040-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73040-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73040-123">CommonParameters</span></span>
<span data-ttu-id="73040-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73040-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73040-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73040-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73040-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73040-126">INPUTS</span></span>

### <span data-ttu-id="73040-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="73040-127">None</span></span>
<span data-ttu-id="73040-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="73040-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73040-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73040-129">OUTPUTS</span></span>

###  
<span data-ttu-id="73040-130">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="73040-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="73040-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="73040-131">NOTES</span></span>

## <span data-ttu-id="73040-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73040-132">RELATED LINKS</span></span>

[<span data-ttu-id="73040-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="73040-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


