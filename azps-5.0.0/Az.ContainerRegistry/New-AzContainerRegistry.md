---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311891"
---
# <span data-ttu-id="86faf-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86faf-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="86faf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86faf-102">SYNOPSIS</span></span>
<span data-ttu-id="86faf-103">Создание реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="86faf-103">Creates a container registry.</span></span>

## <span data-ttu-id="86faf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86faf-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86faf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86faf-105">DESCRIPTION</span></span>
<span data-ttu-id="86faf-106">Командлет New-AzContainerRegistry создает реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="86faf-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="86faf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86faf-107">EXAMPLES</span></span>

### <span data-ttu-id="86faf-108">Пример 1: создание реестра контейнера с помощью новой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="86faf-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="86faf-109">Эта команда создает реестр контейнера с новой учетной записью хранилища в группе ресурсов \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="86faf-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="86faf-110">Пример 2: создание реестра контейнера с включенным пользователем администратора.</span><span class="sxs-lookup"><span data-stu-id="86faf-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="86faf-111">Эта команда создает реестр контейнера с включенным пользователем администратора.</span><span class="sxs-lookup"><span data-stu-id="86faf-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="86faf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86faf-112">PARAMETERS</span></span>

### <span data-ttu-id="86faf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86faf-113">-DefaultProfile</span></span>
<span data-ttu-id="86faf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86faf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86faf-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="86faf-115">-EnableAdminUser</span></span>
<span data-ttu-id="86faf-116">Включите для пользователя администратора контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="86faf-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="86faf-117">-Location</span><span class="sxs-lookup"><span data-stu-id="86faf-117">-Location</span></span>
<span data-ttu-id="86faf-118">Расположение в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="86faf-118">Container Registry Location.</span></span>
<span data-ttu-id="86faf-119">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86faf-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="86faf-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86faf-120">-Name</span></span>
<span data-ttu-id="86faf-121">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="86faf-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="86faf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86faf-122">-ResourceGroupName</span></span>
<span data-ttu-id="86faf-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86faf-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="86faf-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="86faf-124">-Sku</span></span>
<span data-ttu-id="86faf-125">SKU реестра Container.</span><span class="sxs-lookup"><span data-stu-id="86faf-125">Container Registry SKU.</span></span>
<span data-ttu-id="86faf-126">Допустимые значения: Basic.</span><span class="sxs-lookup"><span data-stu-id="86faf-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86faf-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="86faf-127">-Tag</span></span>
<span data-ttu-id="86faf-128">Теги реестра контейнера. пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="86faf-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="86faf-129">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="86faf-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="86faf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86faf-130">-Confirm</span></span>
<span data-ttu-id="86faf-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86faf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86faf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86faf-132">-WhatIf</span></span>
<span data-ttu-id="86faf-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86faf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86faf-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86faf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86faf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86faf-135">CommonParameters</span></span>
<span data-ttu-id="86faf-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86faf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86faf-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86faf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86faf-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86faf-138">INPUTS</span></span>

### <span data-ttu-id="86faf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="86faf-139">System.String</span></span>

## <span data-ttu-id="86faf-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86faf-140">OUTPUTS</span></span>

### <span data-ttu-id="86faf-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86faf-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="86faf-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="86faf-142">NOTES</span></span>

## <span data-ttu-id="86faf-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86faf-143">RELATED LINKS</span></span>

[<span data-ttu-id="86faf-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86faf-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="86faf-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86faf-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="86faf-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86faf-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

