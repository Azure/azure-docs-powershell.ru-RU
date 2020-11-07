---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: d8fb3b740a85b4cb258fcfa08bf9f4e06032fcb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910436"
---
# <span data-ttu-id="06713-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="06713-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="06713-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06713-102">SYNOPSIS</span></span>
<span data-ttu-id="06713-103">Запускает обновление экземпляра VMSS вручную.</span><span class="sxs-lookup"><span data-stu-id="06713-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="06713-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06713-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06713-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06713-105">DESCRIPTION</span></span>
<span data-ttu-id="06713-106">Командлет Update-AzVmssInstance запускает ручное обновление указанного экземпляра установленного набора масштаба виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="06713-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="06713-107">Этот параметр используется, если для политики обновления в VMSS масштабе задано значение "вручную".</span><span class="sxs-lookup"><span data-stu-id="06713-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="06713-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06713-108">EXAMPLES</span></span>

### <span data-ttu-id="06713-109">Пример 1: Начало обновления экземпляра VMSS</span><span class="sxs-lookup"><span data-stu-id="06713-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="06713-110">Эта команда запускает обновление VMSS с именем VMScaleSet001, которое содержит идентификатор экземпляра 0.</span><span class="sxs-lookup"><span data-stu-id="06713-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="06713-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06713-111">PARAMETERS</span></span>

### <span data-ttu-id="06713-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06713-112">-AsJob</span></span>
<span data-ttu-id="06713-113">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="06713-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="06713-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06713-114">-DefaultProfile</span></span>
<span data-ttu-id="06713-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06713-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06713-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="06713-116">-InstanceId</span></span>
<span data-ttu-id="06713-117">Задает в качестве строкового массива идентификатор или идентификаторы экземпляра для обновления.</span><span class="sxs-lookup"><span data-stu-id="06713-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="06713-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06713-118">-ResourceGroupName</span></span>
<span data-ttu-id="06713-119">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="06713-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="06713-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="06713-120">-VMScaleSetName</span></span>
<span data-ttu-id="06713-121">Указывает имя экземпляра VMSS, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="06713-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="06713-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06713-122">-Confirm</span></span>
<span data-ttu-id="06713-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06713-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06713-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06713-124">-WhatIf</span></span>
<span data-ttu-id="06713-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06713-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="06713-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06713-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06713-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06713-127">CommonParameters</span></span>
<span data-ttu-id="06713-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06713-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06713-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06713-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06713-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06713-130">INPUTS</span></span>

### <span data-ttu-id="06713-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="06713-131">None</span></span>
<span data-ttu-id="06713-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="06713-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06713-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06713-133">OUTPUTS</span></span>

###  
<span data-ttu-id="06713-134">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="06713-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="06713-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="06713-135">NOTES</span></span>

## <span data-ttu-id="06713-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06713-136">RELATED LINKS</span></span>

[<span data-ttu-id="06713-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="06713-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


