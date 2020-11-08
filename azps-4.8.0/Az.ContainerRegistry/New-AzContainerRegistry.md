---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 1c546894cf9b11dcb65fb12b9b0575e2fd3191fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236868"
---
# <span data-ttu-id="f880b-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f880b-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="f880b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f880b-102">SYNOPSIS</span></span>
<span data-ttu-id="f880b-103">Создание реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="f880b-103">Creates a container registry.</span></span>

## <span data-ttu-id="f880b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f880b-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f880b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f880b-105">DESCRIPTION</span></span>
<span data-ttu-id="f880b-106">Командлет New-AzContainerRegistry создает реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="f880b-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="f880b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f880b-107">EXAMPLES</span></span>

### <span data-ttu-id="f880b-108">Пример 1: создание реестра контейнера с помощью новой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f880b-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f880b-109">Эта команда создает реестр контейнера с новой учетной записью хранилища в группе ресурсов \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="f880b-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="f880b-110">Пример 2: создание реестра контейнера с включенным пользователем администратора.</span><span class="sxs-lookup"><span data-stu-id="f880b-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f880b-111">Эта команда создает реестр контейнера с включенным пользователем администратора.</span><span class="sxs-lookup"><span data-stu-id="f880b-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="f880b-112">Пример 3: создание реестра контейнера с существующей учетной записью хранения.</span><span class="sxs-lookup"><span data-stu-id="f880b-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f880b-113">Эта команда создает реестр контейнера с существующей учетной записью хранения \` mystorageaccount \` в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="f880b-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="f880b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f880b-114">PARAMETERS</span></span>

### <span data-ttu-id="f880b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f880b-115">-DefaultProfile</span></span>
<span data-ttu-id="f880b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f880b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f880b-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="f880b-117">-EnableAdminUser</span></span>
<span data-ttu-id="f880b-118">Включите для пользователя администратора контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="f880b-118">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f880b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f880b-119">-Location</span></span>
<span data-ttu-id="f880b-120">Расположение в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="f880b-120">Container Registry Location.</span></span>
<span data-ttu-id="f880b-121">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f880b-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="f880b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f880b-122">-Name</span></span>
<span data-ttu-id="f880b-123">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="f880b-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f880b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f880b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f880b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f880b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f880b-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="f880b-126">-Sku</span></span>
<span data-ttu-id="f880b-127">SKU реестра Container.</span><span class="sxs-lookup"><span data-stu-id="f880b-127">Container Registry SKU.</span></span>
<span data-ttu-id="f880b-128">Допустимые значения: Basic.</span><span class="sxs-lookup"><span data-stu-id="f880b-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f880b-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f880b-129">-StorageAccountName</span></span>
<span data-ttu-id="f880b-130">Имя существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f880b-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="f880b-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="f880b-131">-Tag</span></span>
<span data-ttu-id="f880b-132">Теги реестра контейнера. пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="f880b-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="f880b-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="f880b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f880b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f880b-134">-Confirm</span></span>
<span data-ttu-id="f880b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f880b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f880b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f880b-136">-WhatIf</span></span>
<span data-ttu-id="f880b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f880b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f880b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f880b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f880b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f880b-139">CommonParameters</span></span>
<span data-ttu-id="f880b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f880b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f880b-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f880b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f880b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f880b-142">INPUTS</span></span>

### <span data-ttu-id="f880b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f880b-143">System.String</span></span>

## <span data-ttu-id="f880b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f880b-144">OUTPUTS</span></span>

### <span data-ttu-id="f880b-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f880b-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="f880b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f880b-146">NOTES</span></span>

## <span data-ttu-id="f880b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f880b-147">RELATED LINKS</span></span>

[<span data-ttu-id="f880b-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f880b-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="f880b-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f880b-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="f880b-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f880b-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

