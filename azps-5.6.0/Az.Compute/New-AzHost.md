---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: adeee59745aa3f14fe3b5580139b17412e496f0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959683"
---
# <span data-ttu-id="4e171-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="4e171-101">New-AzHost</span></span>

## <span data-ttu-id="4e171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e171-102">SYNOPSIS</span></span>
<span data-ttu-id="4e171-103">Создает хост.</span><span class="sxs-lookup"><span data-stu-id="4e171-103">Creates a  host.</span></span>

## <span data-ttu-id="4e171-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e171-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e171-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e171-105">DESCRIPTION</span></span>
<span data-ttu-id="4e171-106">Этот cmdlet создаст host (Хост).</span><span class="sxs-lookup"><span data-stu-id="4e171-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="4e171-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e171-107">EXAMPLES</span></span>

### <span data-ttu-id="4e171-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e171-108">Example 1</span></span>
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

<span data-ttu-id="4e171-109">Эта команда создает хост заданного SKU в заданной группе хостов и заданном расположении.</span><span class="sxs-lookup"><span data-stu-id="4e171-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="4e171-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e171-110">PARAMETERS</span></span>

### <span data-ttu-id="4e171-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e171-111">-AsJob</span></span>
<span data-ttu-id="4e171-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4e171-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e171-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="4e171-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="4e171-114">Определяет, следует ли автоматически заменять хост в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="4e171-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="4e171-115">Значение по умолчанию имеет значение ИСТИНА, если не предоставлено.</span><span class="sxs-lookup"><span data-stu-id="4e171-115">The value is defaulted to 'true' when not provided.</span></span>

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

### <span data-ttu-id="4e171-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e171-116">-DefaultProfile</span></span>
<span data-ttu-id="4e171-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e171-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e171-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="4e171-118">-HostGroupName</span></span>
<span data-ttu-id="4e171-119">Указывает имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="4e171-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="4e171-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4e171-120">-LicenseType</span></span>
<span data-ttu-id="4e171-121">Указывает тип лицензии на программное обеспечение, который будет применяться к ВМ-машин, развернутых на размещении.</span><span class="sxs-lookup"><span data-stu-id="4e171-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="4e171-122">Возможные значения: Нет, Windows_Server_Hybrid и Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="4e171-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="4e171-123">Значение по умолчанию — "Нет".</span><span class="sxs-lookup"><span data-stu-id="4e171-123">Default value is None.</span></span>

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

### <span data-ttu-id="4e171-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4e171-124">-Location</span></span>
<span data-ttu-id="4e171-125">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="4e171-125">Specifies the location.</span></span>

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

### <span data-ttu-id="4e171-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4e171-126">-Name</span></span>
<span data-ttu-id="4e171-127">Указывает имя хоста.</span><span class="sxs-lookup"><span data-stu-id="4e171-127">Specifies the name of the host.</span></span>

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

### <span data-ttu-id="4e171-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="4e171-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="4e171-129">Определяет количество домена неисправности платформы для хоста.</span><span class="sxs-lookup"><span data-stu-id="4e171-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="4e171-130">Минимальное значение — 0, максимальное — 2.</span><span class="sxs-lookup"><span data-stu-id="4e171-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="4e171-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e171-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e171-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e171-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e171-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="4e171-133">-Sku</span></span>
<span data-ttu-id="4e171-134">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="4e171-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="4e171-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e171-135">-Tag</span></span>
<span data-ttu-id="4e171-136">Определяет теги.</span><span class="sxs-lookup"><span data-stu-id="4e171-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="4e171-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e171-137">-Confirm</span></span>
<span data-ttu-id="4e171-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e171-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e171-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e171-139">-WhatIf</span></span>
<span data-ttu-id="4e171-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e171-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e171-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e171-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e171-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e171-142">CommonParameters</span></span>
<span data-ttu-id="4e171-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e171-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e171-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e171-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e171-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e171-145">INPUTS</span></span>

### <span data-ttu-id="4e171-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4e171-146">System.String</span></span>

## <span data-ttu-id="4e171-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e171-147">OUTPUTS</span></span>

### <span data-ttu-id="4e171-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="4e171-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="4e171-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e171-149">NOTES</span></span>

## <span data-ttu-id="4e171-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e171-150">RELATED LINKS</span></span>
