---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
ms.openlocfilehash: 49e8e5aeddba1b15c97155a200413ea774c8a7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250187"
---
# <span data-ttu-id="4b517-101">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4b517-101">Update-AzManagedHsm</span></span>

## <span data-ttu-id="4b517-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b517-102">SYNOPSIS</span></span>
<span data-ttu-id="4b517-103">Обновите состояние управляемого HSM для Azure.</span><span class="sxs-lookup"><span data-stu-id="4b517-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="4b517-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b517-104">SYNTAX</span></span>

### <span data-ttu-id="4b517-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b517-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b517-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b517-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b517-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b517-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b517-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b517-108">DESCRIPTION</span></span>
<span data-ttu-id="4b517-109">Этот командлет обновляет состояние управляемого HSM для Azure.</span><span class="sxs-lookup"><span data-stu-id="4b517-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="4b517-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b517-110">EXAMPLES</span></span>

### <span data-ttu-id="4b517-111">Пример 1: обновление управляемого HSM-кода напрямую</span><span class="sxs-lookup"><span data-stu-id="4b517-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

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

<span data-ttu-id="4b517-112">Обновляет Теги управляемого HSM, именуемого `$hsmName` в группе ресурсов `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="4b517-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="4b517-113">Пример 2: обновление управляемого HSM-кода с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="4b517-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="4b517-114">Обновляет Теги управляемого HSM с помощью синтаксиса трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="4b517-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="4b517-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b517-115">PARAMETERS</span></span>

### <span data-ttu-id="4b517-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b517-116">-DefaultProfile</span></span>
<span data-ttu-id="4b517-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b517-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b517-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b517-118">-InputObject</span></span>
<span data-ttu-id="4b517-119">Управляемый объект HSM.</span><span class="sxs-lookup"><span data-stu-id="4b517-119">Managed HSM object.</span></span>

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

### <span data-ttu-id="4b517-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4b517-120">-Name</span></span>
<span data-ttu-id="4b517-121">Имя управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="4b517-121">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="4b517-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b517-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b517-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b517-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="4b517-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b517-124">-ResourceId</span></span>
<span data-ttu-id="4b517-125">Идентификатор ресурса управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="4b517-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="4b517-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="4b517-126">-Tag</span></span>
<span data-ttu-id="4b517-127">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b517-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4b517-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b517-128">-Confirm</span></span>
<span data-ttu-id="4b517-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b517-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b517-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b517-130">-WhatIf</span></span>
<span data-ttu-id="4b517-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b517-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b517-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b517-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b517-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b517-133">CommonParameters</span></span>
<span data-ttu-id="4b517-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b517-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b517-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b517-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b517-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b517-136">INPUTS</span></span>

### <span data-ttu-id="4b517-137">Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4b517-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="4b517-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4b517-138">System.String</span></span>

### <span data-ttu-id="4b517-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4b517-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4b517-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b517-140">OUTPUTS</span></span>

### <span data-ttu-id="4b517-141">Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4b517-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="4b517-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b517-142">NOTES</span></span>

## <span data-ttu-id="4b517-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b517-143">RELATED LINKS</span></span>

[<span data-ttu-id="4b517-144">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4b517-144">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="4b517-145">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4b517-145">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="4b517-146">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4b517-146">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)