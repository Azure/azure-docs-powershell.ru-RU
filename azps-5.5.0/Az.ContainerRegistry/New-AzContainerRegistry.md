---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215524"
---
# <span data-ttu-id="c6a36-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c6a36-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="c6a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a36-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a36-103">Создает реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="c6a36-103">Creates a container registry.</span></span>

## <span data-ttu-id="c6a36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6a36-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6a36-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6a36-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a36-106">С New-AzContainerRegistry создается реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="c6a36-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="c6a36-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6a36-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a36-108">Пример 1. Создание реестра контейнера с новой учетной записью хранения.</span><span class="sxs-lookup"><span data-stu-id="c6a36-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c6a36-109">Эта команда создает реестр контейнера с новой учетной записью хранения в группе ресурсов \` MyResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="c6a36-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="c6a36-110">Пример 2. Создание реестра контейнера с включенным пользователем-администратором.</span><span class="sxs-lookup"><span data-stu-id="c6a36-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c6a36-111">Эта команда создает реестр контейнера с включенным пользователем-администратором.</span><span class="sxs-lookup"><span data-stu-id="c6a36-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="c6a36-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6a36-112">PARAMETERS</span></span>

### <span data-ttu-id="c6a36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a36-113">-DefaultProfile</span></span>
<span data-ttu-id="c6a36-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c6a36-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6a36-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="c6a36-115">-EnableAdminUser</span></span>
<span data-ttu-id="c6a36-116">Включить пользователя администратора для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="c6a36-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="c6a36-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c6a36-117">-Location</span></span>
<span data-ttu-id="c6a36-118">Расположение реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="c6a36-118">Container Registry Location.</span></span>
<span data-ttu-id="c6a36-119">Расположение группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6a36-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c6a36-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c6a36-120">-Name</span></span>
<span data-ttu-id="c6a36-121">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="c6a36-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="c6a36-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a36-122">-ResourceGroupName</span></span>
<span data-ttu-id="c6a36-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6a36-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6a36-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="c6a36-124">-Sku</span></span>
<span data-ttu-id="c6a36-125">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="c6a36-125">Container Registry SKU.</span></span>
<span data-ttu-id="c6a36-126">Разрешенные значения: базовый.</span><span class="sxs-lookup"><span data-stu-id="c6a36-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="c6a36-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6a36-127">-Tag</span></span>
<span data-ttu-id="c6a36-128">Пары "Теги.Ключ - значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="c6a36-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="c6a36-129">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c6a36-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c6a36-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6a36-130">-Confirm</span></span>
<span data-ttu-id="c6a36-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c6a36-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6a36-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a36-132">-WhatIf</span></span>
<span data-ttu-id="c6a36-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6a36-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6a36-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c6a36-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6a36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a36-135">CommonParameters</span></span>
<span data-ttu-id="c6a36-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a36-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6a36-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a36-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6a36-138">INPUTS</span></span>

### <span data-ttu-id="c6a36-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a36-139">System.String</span></span>

## <span data-ttu-id="c6a36-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6a36-140">OUTPUTS</span></span>

### <span data-ttu-id="c6a36-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c6a36-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c6a36-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6a36-142">NOTES</span></span>

## <span data-ttu-id="c6a36-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6a36-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6a36-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c6a36-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="c6a36-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c6a36-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="c6a36-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c6a36-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

