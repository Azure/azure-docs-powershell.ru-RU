---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215492"
---
# <span data-ttu-id="7842c-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7842c-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="7842c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7842c-102">SYNOPSIS</span></span>
<span data-ttu-id="7842c-103">Обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="7842c-103">Updates a container registry.</span></span>

## <span data-ttu-id="7842c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7842c-104">SYNTAX</span></span>

### <span data-ttu-id="7842c-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7842c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7842c-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7842c-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7842c-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7842c-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7842c-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7842c-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7842c-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7842c-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7842c-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7842c-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7842c-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7842c-111">DESCRIPTION</span></span>
<span data-ttu-id="7842c-112">Новый Update-AzContainerRegistry обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="7842c-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="7842c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7842c-113">EXAMPLES</span></span>

### <span data-ttu-id="7842c-114">Пример 1. Enable admin user for a specified container registry</span><span class="sxs-lookup"><span data-stu-id="7842c-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="7842c-115">Эта команда позволяет администратору использовать указанный реестр контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7842c-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="7842c-116">Пример 2. Настройка учетной записи хранения, используемой указанным реестром контейнеров</span><span class="sxs-lookup"><span data-stu-id="7842c-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="7842c-117">Эта команда задает для указанного реестра контейнера существующую учетную запись хранения \` mystorageaccount \` в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="7842c-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="7842c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7842c-118">PARAMETERS</span></span>

### <span data-ttu-id="7842c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7842c-119">-DefaultProfile</span></span>
<span data-ttu-id="7842c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7842c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7842c-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="7842c-121">-DisableAdminUser</span></span>
<span data-ttu-id="7842c-122">Включить пользователя администратора для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7842c-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="7842c-123">-EnableAdminUser</span></span>
<span data-ttu-id="7842c-124">Включить пользователя администратора для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7842c-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7842c-125">-Name</span></span>
<span data-ttu-id="7842c-126">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7842c-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7842c-127">-NetworkRuleSet</span></span>
<span data-ttu-id="7842c-128">Сетевое правило для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7842c-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7842c-129">-ResourceGroupName</span></span>
<span data-ttu-id="7842c-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7842c-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7842c-131">-ResourceId</span></span>
<span data-ttu-id="7842c-132">ИД контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="7842c-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="7842c-133">-Sku</span></span>
<span data-ttu-id="7842c-134">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="7842c-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7842c-135">-StorageAccountName</span></span>
<span data-ttu-id="7842c-136">Имя существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7842c-136">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="7842c-137">-Tag</span></span>
<span data-ttu-id="7842c-138">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="7842c-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="7842c-139">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7842c-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7842c-140">-Confirm</span></span>
<span data-ttu-id="7842c-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7842c-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7842c-142">-WhatIf</span></span>
<span data-ttu-id="7842c-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7842c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7842c-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7842c-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7842c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7842c-145">CommonParameters</span></span>
<span data-ttu-id="7842c-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7842c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7842c-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7842c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7842c-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7842c-148">INPUTS</span></span>

### <span data-ttu-id="7842c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7842c-149">System.String</span></span>

## <span data-ttu-id="7842c-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7842c-150">OUTPUTS</span></span>

### <span data-ttu-id="7842c-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7842c-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="7842c-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7842c-152">NOTES</span></span>

## <span data-ttu-id="7842c-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7842c-153">RELATED LINKS</span></span>

[<span data-ttu-id="7842c-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7842c-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="7842c-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7842c-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="7842c-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7842c-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

