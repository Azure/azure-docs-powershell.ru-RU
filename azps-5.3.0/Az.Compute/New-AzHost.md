---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519585"
---
# <span data-ttu-id="9f1c8-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="9f1c8-101">New-AzHost</span></span>

## <span data-ttu-id="9f1c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f1c8-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1c8-103">Создает хост.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-103">Creates a  host.</span></span>

## <span data-ttu-id="9f1c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f1c8-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f1c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f1c8-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1c8-106">Этот cmdlet создаст host (Хост).</span><span class="sxs-lookup"><span data-stu-id="9f1c8-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="9f1c8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f1c8-107">EXAMPLES</span></span>

### <span data-ttu-id="9f1c8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f1c8-108">Example 1</span></span>
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

<span data-ttu-id="9f1c8-109">Эта команда создает хост заданного SKU в заданной группе хостов и заданном расположении.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="9f1c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f1c8-110">PARAMETERS</span></span>

### <span data-ttu-id="9f1c8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f1c8-111">-AsJob</span></span>
<span data-ttu-id="9f1c8-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9f1c8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f1c8-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="9f1c8-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="9f1c8-114">Указывает, следует ли автоматически заменять хост в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="9f1c8-115">Если не предоставлено значение, это значение по умолчанию имеет значение ИСТИНА.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-115">The value is defaulted to 'true' when not provided.</span></span>

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

### <span data-ttu-id="9f1c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1c8-116">-DefaultProfile</span></span>
<span data-ttu-id="9f1c8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f1c8-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1c8-118">-HostGroupName</span></span>
<span data-ttu-id="9f1c8-119">Указывает имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="9f1c8-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9f1c8-120">-LicenseType</span></span>
<span data-ttu-id="9f1c8-121">Указывает тип лицензии на программное обеспечение, который будет применяться к ВМ-машин, развернутых на хосте.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="9f1c8-122">Возможные значения: Нет, Windows_Server_Hybrid и Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="9f1c8-123">Значение по умолчанию — "Нет".</span><span class="sxs-lookup"><span data-stu-id="9f1c8-123">Default value is None.</span></span>

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

### <span data-ttu-id="9f1c8-124">-Location</span><span class="sxs-lookup"><span data-stu-id="9f1c8-124">-Location</span></span>
<span data-ttu-id="9f1c8-125">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-125">Specifies the location.</span></span>

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

### <span data-ttu-id="9f1c8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9f1c8-126">-Name</span></span>
<span data-ttu-id="9f1c8-127">Указывает имя хоста.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-127">Specifies the name of the host.</span></span>

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

### <span data-ttu-id="9f1c8-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="9f1c8-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="9f1c8-129">Определяет количество домена неисправности платформы для хоста.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="9f1c8-130">Минимальное значение — 0, а максимальное — 2.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="9f1c8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1c8-131">-ResourceGroupName</span></span>
<span data-ttu-id="9f1c8-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f1c8-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="9f1c8-133">-Sku</span></span>
<span data-ttu-id="9f1c8-134">Указывает имя SKU.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="9f1c8-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f1c8-135">-Tag</span></span>
<span data-ttu-id="9f1c8-136">Определяет теги.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="9f1c8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f1c8-137">-Confirm</span></span>
<span data-ttu-id="9f1c8-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f1c8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f1c8-139">-WhatIf</span></span>
<span data-ttu-id="9f1c8-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f1c8-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f1c8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1c8-142">CommonParameters</span></span>
<span data-ttu-id="9f1c8-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1c8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1c8-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f1c8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1c8-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f1c8-145">INPUTS</span></span>

### <span data-ttu-id="9f1c8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9f1c8-146">System.String</span></span>

## <span data-ttu-id="9f1c8-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f1c8-147">OUTPUTS</span></span>

### <span data-ttu-id="9f1c8-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="9f1c8-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="9f1c8-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f1c8-149">NOTES</span></span>

## <span data-ttu-id="9f1c8-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f1c8-150">RELATED LINKS</span></span>
