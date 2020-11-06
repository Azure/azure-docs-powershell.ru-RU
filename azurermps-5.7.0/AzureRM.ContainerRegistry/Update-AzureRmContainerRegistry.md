---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565549"
---
# <span data-ttu-id="4293c-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4293c-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="4293c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4293c-102">SYNOPSIS</span></span>
<span data-ttu-id="4293c-103">Обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="4293c-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4293c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4293c-104">SYNTAX</span></span>

### <span data-ttu-id="4293c-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4293c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4293c-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4293c-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4293c-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4293c-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4293c-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4293c-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4293c-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4293c-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4293c-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4293c-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4293c-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4293c-111">DESCRIPTION</span></span>
<span data-ttu-id="4293c-112">Командлет Update-AzureRmContainerRegistry обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="4293c-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="4293c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4293c-113">EXAMPLES</span></span>

### <span data-ttu-id="4293c-114">Пример 1: включение учетной записи пользователя администратора для указанного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="4293c-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="4293c-115">Эта команда позволяет пользователю администратора для указанного контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="4293c-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="4293c-116">Пример 2: Настройка учетной записи хранения, используемой в указанном контейнере реестра</span><span class="sxs-lookup"><span data-stu-id="4293c-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="4293c-117">Эта команда задает для указанного контейнера реестра использование существующей учетной записи хранения \` mystorageaccount \` в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="4293c-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="4293c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4293c-118">PARAMETERS</span></span>

### <span data-ttu-id="4293c-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="4293c-119">-DisableAdminUser</span></span>
<span data-ttu-id="4293c-120">Включите для пользователя администратора контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="4293c-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="4293c-121">-EnableAdminUser</span></span>
<span data-ttu-id="4293c-122">Включите для пользователя администратора контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="4293c-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4293c-123">-Name</span></span>
<span data-ttu-id="4293c-124">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="4293c-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4293c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4293c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4293c-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4293c-127">-StorageAccountName</span></span>
<span data-ttu-id="4293c-128">Имя существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4293c-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="4293c-129">-Tag</span></span>
<span data-ttu-id="4293c-130">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="4293c-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="4293c-131">Например:</span><span class="sxs-lookup"><span data-stu-id="4293c-131">For example:</span></span>

<span data-ttu-id="4293c-132">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4293c-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4293c-133">-Confirm</span></span>
<span data-ttu-id="4293c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4293c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4293c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4293c-135">-WhatIf</span></span>
<span data-ttu-id="4293c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4293c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4293c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4293c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4293c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4293c-138">-DefaultProfile</span></span>
<span data-ttu-id="4293c-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4293c-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4293c-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4293c-140">-ResourceId</span></span>
<span data-ttu-id="4293c-141">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="4293c-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="4293c-142">-Sku</span></span>
<span data-ttu-id="4293c-143">SKU реестра Container.</span><span class="sxs-lookup"><span data-stu-id="4293c-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4293c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4293c-144">CommonParameters</span></span>
<span data-ttu-id="4293c-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4293c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4293c-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4293c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4293c-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4293c-147">INPUTS</span></span>

### <span data-ttu-id="4293c-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="4293c-148">None</span></span>
<span data-ttu-id="4293c-149">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4293c-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4293c-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4293c-150">OUTPUTS</span></span>

### <span data-ttu-id="4293c-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4293c-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="4293c-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="4293c-152">NOTES</span></span>

## <span data-ttu-id="4293c-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4293c-153">RELATED LINKS</span></span>

[<span data-ttu-id="4293c-154">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4293c-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="4293c-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4293c-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="4293c-156">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4293c-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

