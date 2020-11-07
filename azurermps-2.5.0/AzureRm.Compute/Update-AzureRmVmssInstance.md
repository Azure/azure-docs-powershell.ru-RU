---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
ms.openlocfilehash: 07b068587848bc8af92fc49b039155c0a2c4fdd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914501"
---
# <span data-ttu-id="36b74-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="36b74-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="36b74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36b74-102">SYNOPSIS</span></span>
<span data-ttu-id="36b74-103">Запускает обновление экземпляра VMSS вручную.</span><span class="sxs-lookup"><span data-stu-id="36b74-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36b74-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36b74-105">DESCRIPTION</span></span>
<span data-ttu-id="36b74-106">Командлет Update-AzureRmVmssInstance запускает ручное обновление указанного экземпляра установленного набора масштаба виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="36b74-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="36b74-107">Этот параметр используется, если для политики обновления в VMSS масштабе задано значение "вручную".</span><span class="sxs-lookup"><span data-stu-id="36b74-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="36b74-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36b74-108">EXAMPLES</span></span>

### <span data-ttu-id="36b74-109">Пример 1: Начало обновления экземпляра VMSS</span><span class="sxs-lookup"><span data-stu-id="36b74-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="36b74-110">Эта команда запускает обновление VMSS с именем VMScaleSet001, которое содержит идентификатор экземпляра 0.</span><span class="sxs-lookup"><span data-stu-id="36b74-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="36b74-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36b74-111">PARAMETERS</span></span>

### <span data-ttu-id="36b74-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36b74-112">-AsJob</span></span>
<span data-ttu-id="36b74-113">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="36b74-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="36b74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b74-114">-DefaultProfile</span></span>
<span data-ttu-id="36b74-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36b74-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36b74-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="36b74-116">-InstanceId</span></span>
<span data-ttu-id="36b74-117">Задает в качестве строкового массива идентификатор или идентификаторы экземпляра для обновления.</span><span class="sxs-lookup"><span data-stu-id="36b74-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="36b74-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b74-118">-ResourceGroupName</span></span>
<span data-ttu-id="36b74-119">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="36b74-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="36b74-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36b74-120">-VMScaleSetName</span></span>
<span data-ttu-id="36b74-121">Указывает имя экземпляра VMSS, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="36b74-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="36b74-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36b74-122">-Confirm</span></span>
<span data-ttu-id="36b74-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36b74-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b74-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b74-124">-WhatIf</span></span>
<span data-ttu-id="36b74-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36b74-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="36b74-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36b74-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b74-127">CommonParameters</span></span>
<span data-ttu-id="36b74-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36b74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b74-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b74-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b74-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36b74-130">INPUTS</span></span>

### <span data-ttu-id="36b74-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="36b74-131">None</span></span>
<span data-ttu-id="36b74-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="36b74-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36b74-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36b74-133">OUTPUTS</span></span>

###  
<span data-ttu-id="36b74-134">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36b74-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="36b74-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="36b74-135">NOTES</span></span>

## <span data-ttu-id="36b74-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36b74-136">RELATED LINKS</span></span>

[<span data-ttu-id="36b74-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36b74-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


