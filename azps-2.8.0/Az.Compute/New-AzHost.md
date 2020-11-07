---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: e10e60845c9aeb90b7c708a65f7d681d9894b022
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721846"
---
# <span data-ttu-id="c17e2-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="c17e2-101">New-AzHost</span></span>

## <span data-ttu-id="c17e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c17e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c17e2-103">Создание узла.</span><span class="sxs-lookup"><span data-stu-id="c17e2-103">Creates a  host.</span></span>

## <span data-ttu-id="c17e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c17e2-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c17e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c17e2-105">DESCRIPTION</span></span>
<span data-ttu-id="c17e2-106">Этот командлет создаст узел.</span><span class="sxs-lookup"><span data-stu-id="c17e2-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="c17e2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c17e2-107">EXAMPLES</span></span>

### <span data-ttu-id="c17e2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c17e2-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="c17e2-109">Эта команда создает узел заданного SKU в заданной группе узлов и указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="c17e2-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="c17e2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c17e2-110">PARAMETERS</span></span>

### <span data-ttu-id="c17e2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c17e2-111">-AsJob</span></span>
<span data-ttu-id="c17e2-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c17e2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c17e2-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="c17e2-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="c17e2-114">Указывает, следует ли автоматически заменять узел в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="c17e2-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="c17e2-115">Значение по умолчанию — "истина", если не указано.</span><span class="sxs-lookup"><span data-stu-id="c17e2-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17e2-116">-DefaultProfile</span></span>
<span data-ttu-id="c17e2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c17e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c17e2-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="c17e2-118">-HostGroupName</span></span>
<span data-ttu-id="c17e2-119">Указывает имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="c17e2-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="c17e2-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c17e2-120">-LicenseType</span></span>
<span data-ttu-id="c17e2-121">Указывает тип лицензии на программное обеспечение, которая будет применяться к виртуальным машинам, развернутым на узле.</span><span class="sxs-lookup"><span data-stu-id="c17e2-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="c17e2-122">Возможные значения: None, Windows_Server_Hybrid и Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="c17e2-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="c17e2-123">Значение по умолчанию — None (нет).</span><span class="sxs-lookup"><span data-stu-id="c17e2-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-124">-Location</span><span class="sxs-lookup"><span data-stu-id="c17e2-124">-Location</span></span>
<span data-ttu-id="c17e2-125">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="c17e2-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c17e2-126">-Name</span></span>
<span data-ttu-id="c17e2-127">Указывает имя узла.</span><span class="sxs-lookup"><span data-stu-id="c17e2-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="c17e2-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="c17e2-129">Указывает количество доменов сбоев платформы узла.</span><span class="sxs-lookup"><span data-stu-id="c17e2-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="c17e2-130">Затем минимальное значение равно 0 и максимальное значение равно 2.</span><span class="sxs-lookup"><span data-stu-id="c17e2-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c17e2-131">-ResourceGroupName</span></span>
<span data-ttu-id="c17e2-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c17e2-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="c17e2-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="c17e2-133">-Sku</span></span>
<span data-ttu-id="c17e2-134">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="c17e2-134">Specifies the name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="c17e2-135">-Tag</span></span>
<span data-ttu-id="c17e2-136">Указывает Теги.</span><span class="sxs-lookup"><span data-stu-id="c17e2-136">Specifies Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c17e2-137">-Confirm</span></span>
<span data-ttu-id="c17e2-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c17e2-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c17e2-139">-WhatIf</span></span>
<span data-ttu-id="c17e2-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c17e2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c17e2-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c17e2-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17e2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17e2-142">CommonParameters</span></span>
<span data-ttu-id="c17e2-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c17e2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17e2-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c17e2-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17e2-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c17e2-145">INPUTS</span></span>

### <span data-ttu-id="c17e2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c17e2-146">System.String</span></span>

## <span data-ttu-id="c17e2-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c17e2-147">OUTPUTS</span></span>

### <span data-ttu-id="c17e2-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="c17e2-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="c17e2-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="c17e2-149">NOTES</span></span>

## <span data-ttu-id="c17e2-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c17e2-150">RELATED LINKS</span></span>
