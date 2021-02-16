---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8a4c55f8b823a72224dc658a3ddc37ee867d781b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219452"
---
# <span data-ttu-id="38a7d-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="38a7d-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="38a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="38a7d-103">Обновление состояния службы HSM, управляемой Azure.</span><span class="sxs-lookup"><span data-stu-id="38a7d-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="38a7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38a7d-104">SYNTAX</span></span>

### <span data-ttu-id="38a7d-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38a7d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38a7d-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38a7d-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38a7d-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38a7d-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38a7d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38a7d-108">DESCRIPTION</span></span>
<span data-ttu-id="38a7d-109">Этот cmdlet обновляет состояние службы управления HSM Azure.</span><span class="sxs-lookup"><span data-stu-id="38a7d-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="38a7d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38a7d-110">EXAMPLES</span></span>

### <span data-ttu-id="38a7d-111">Пример 1. Обновление управляемого HSM напрямую</span><span class="sxs-lookup"><span data-stu-id="38a7d-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="38a7d-112">Обновляет теги управляемого HSM в `$hsmName` группе `$resourceGroupName` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38a7d-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="38a7d-113">Пример 2. Обновление управляемого HSM с помощью piping</span><span class="sxs-lookup"><span data-stu-id="38a7d-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="38a7d-114">Обновляет теги управляемого HSM с помощью синтаксиса piping.</span><span class="sxs-lookup"><span data-stu-id="38a7d-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="38a7d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38a7d-115">PARAMETERS</span></span>

### <span data-ttu-id="38a7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a7d-116">-DefaultProfile</span></span>
<span data-ttu-id="38a7d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38a7d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a7d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38a7d-118">-InputObject</span></span>
<span data-ttu-id="38a7d-119">Управляемый объект HSM.</span><span class="sxs-lookup"><span data-stu-id="38a7d-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38a7d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="38a7d-120">-Name</span></span>
<span data-ttu-id="38a7d-121">Имя управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="38a7d-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="38a7d-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38a7d-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a7d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38a7d-124">-ResourceId</span></span>
<span data-ttu-id="38a7d-125">ИД ресурса управляемой HSM.</span><span class="sxs-lookup"><span data-stu-id="38a7d-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a7d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="38a7d-126">-Tag</span></span>
<span data-ttu-id="38a7d-127">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="38a7d-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a7d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38a7d-128">-Confirm</span></span>
<span data-ttu-id="38a7d-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a7d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38a7d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a7d-130">-WhatIf</span></span>
<span data-ttu-id="38a7d-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a7d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a7d-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38a7d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38a7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a7d-133">CommonParameters</span></span>
<span data-ttu-id="38a7d-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a7d-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38a7d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a7d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38a7d-136">INPUTS</span></span>

### <span data-ttu-id="38a7d-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="38a7d-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="38a7d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="38a7d-138">System.String</span></span>

### <span data-ttu-id="38a7d-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="38a7d-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="38a7d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38a7d-140">OUTPUTS</span></span>

### <span data-ttu-id="38a7d-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="38a7d-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="38a7d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38a7d-142">NOTES</span></span>

## <span data-ttu-id="38a7d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38a7d-143">RELATED LINKS</span></span>

[<span data-ttu-id="38a7d-144">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="38a7d-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="38a7d-145">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="38a7d-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="38a7d-146">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="38a7d-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)