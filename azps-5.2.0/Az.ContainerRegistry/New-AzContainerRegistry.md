---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405111"
---
# <span data-ttu-id="1673b-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1673b-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="1673b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1673b-102">SYNOPSIS</span></span>
<span data-ttu-id="1673b-103">Создает реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="1673b-103">Creates a container registry.</span></span>

## <span data-ttu-id="1673b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1673b-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1673b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1673b-105">DESCRIPTION</span></span>
<span data-ttu-id="1673b-106">С New-AzContainerRegistry создается реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="1673b-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="1673b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1673b-107">EXAMPLES</span></span>

### <span data-ttu-id="1673b-108">Пример 1. Создание реестра контейнеров с новой учетной записью хранения.</span><span class="sxs-lookup"><span data-stu-id="1673b-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="1673b-109">Эта команда создает реестр контейнера с новой учетной записью хранения в группе ресурсов \` MyResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="1673b-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="1673b-110">Пример 2. Создание реестра контейнера с включенным пользователем-администратором.</span><span class="sxs-lookup"><span data-stu-id="1673b-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="1673b-111">Эта команда создает реестр контейнера с включенным пользователем-администратором.</span><span class="sxs-lookup"><span data-stu-id="1673b-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="1673b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1673b-112">PARAMETERS</span></span>

### <span data-ttu-id="1673b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1673b-113">-DefaultProfile</span></span>
<span data-ttu-id="1673b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1673b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1673b-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1673b-115">-EnableAdminUser</span></span>
<span data-ttu-id="1673b-116">Включить пользователя администратора для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="1673b-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="1673b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="1673b-117">-Location</span></span>
<span data-ttu-id="1673b-118">Расположение реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="1673b-118">Container Registry Location.</span></span>
<span data-ttu-id="1673b-119">Расположение группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1673b-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="1673b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1673b-120">-Name</span></span>
<span data-ttu-id="1673b-121">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="1673b-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="1673b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1673b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1673b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1673b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="1673b-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="1673b-124">-Sku</span></span>
<span data-ttu-id="1673b-125">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="1673b-125">Container Registry SKU.</span></span>
<span data-ttu-id="1673b-126">Разрешенные значения: базовые.</span><span class="sxs-lookup"><span data-stu-id="1673b-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="1673b-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="1673b-127">-Tag</span></span>
<span data-ttu-id="1673b-128">Пары "теги.ключ- значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="1673b-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="1673b-129">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1673b-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1673b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1673b-130">-Confirm</span></span>
<span data-ttu-id="1673b-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1673b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1673b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1673b-132">-WhatIf</span></span>
<span data-ttu-id="1673b-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1673b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1673b-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1673b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1673b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1673b-135">CommonParameters</span></span>
<span data-ttu-id="1673b-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1673b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1673b-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1673b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1673b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1673b-138">INPUTS</span></span>

### <span data-ttu-id="1673b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1673b-139">System.String</span></span>

## <span data-ttu-id="1673b-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1673b-140">OUTPUTS</span></span>

### <span data-ttu-id="1673b-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1673b-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="1673b-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1673b-142">NOTES</span></span>

## <span data-ttu-id="1673b-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1673b-143">RELATED LINKS</span></span>

[<span data-ttu-id="1673b-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1673b-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="1673b-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1673b-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="1673b-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1673b-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

