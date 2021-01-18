---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507213"
---
# <span data-ttu-id="aae32-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="aae32-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="aae32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aae32-102">SYNOPSIS</span></span>
<span data-ttu-id="aae32-103">Получите управляемые HSMs.</span><span class="sxs-lookup"><span data-stu-id="aae32-103">Get managed HSMs.</span></span>

## <span data-ttu-id="aae32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aae32-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aae32-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aae32-105">DESCRIPTION</span></span>
<span data-ttu-id="aae32-106">**Cmdlet Get-AzKeyVaultManagedHsm** получает сведения об управляемых HSMs в подписке.</span><span class="sxs-lookup"><span data-stu-id="aae32-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="aae32-107">Вы можете просмотреть все управляемые HSMs-экземпляры в подписке или отфильтровать результаты по группе ресурсов или определенной управляемой службе управления HSM.</span><span class="sxs-lookup"><span data-stu-id="aae32-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="aae32-108">Имейте в виду, что хотя при работе с одним управляемым HSM-решением указать группу ресурсов необязательно, это следует сделать для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="aae32-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="aae32-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aae32-109">EXAMPLES</span></span>

### <span data-ttu-id="aae32-110">Пример 1. Все управляемые HSMs в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="aae32-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="aae32-111">Эта команда получает все управляемые HSMs в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="aae32-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="aae32-112">Пример 2. Получить Управлили HSM</span><span class="sxs-lookup"><span data-stu-id="aae32-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="aae32-113">Эта команда получает управляемый HSM-сервис с именем myhsm в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="aae32-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="aae32-114">Пример 3. Управление HSMs в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="aae32-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="aae32-115">Эта команда получает все управляемые HSMs в группе ресурсов myrg1.</span><span class="sxs-lookup"><span data-stu-id="aae32-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="aae32-116">Пример 4. Управление HSMs с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="aae32-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="aae32-117">Эта команда получает все управляемые HSMs в подписке, которая начинается с "myhsm".</span><span class="sxs-lookup"><span data-stu-id="aae32-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="aae32-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aae32-118">PARAMETERS</span></span>

### <span data-ttu-id="aae32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae32-119">-DefaultProfile</span></span>
<span data-ttu-id="aae32-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aae32-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aae32-121">-Name</span><span class="sxs-lookup"><span data-stu-id="aae32-121">-Name</span></span>
<span data-ttu-id="aae32-122">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="aae32-122">HSM name.</span></span> <span data-ttu-id="aae32-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="aae32-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="aae32-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae32-124">-ResourceGroupName</span></span>
<span data-ttu-id="aae32-125">Указывает имя группы ресурсов, связанной с управляемым HSM-запросом.</span><span class="sxs-lookup"><span data-stu-id="aae32-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="aae32-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="aae32-126">-Tag</span></span>
<span data-ttu-id="aae32-127">Указывает ключ и необязательное значение указанного тега для фильтрации списка управляемых сообщений HSMs по.</span><span class="sxs-lookup"><span data-stu-id="aae32-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae32-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae32-128">CommonParameters</span></span>
<span data-ttu-id="aae32-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae32-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae32-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aae32-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae32-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aae32-131">INPUTS</span></span>

### <span data-ttu-id="aae32-132">System.String</span><span class="sxs-lookup"><span data-stu-id="aae32-132">System.String</span></span>

### <span data-ttu-id="aae32-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aae32-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aae32-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aae32-134">OUTPUTS</span></span>

### <span data-ttu-id="aae32-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="aae32-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="aae32-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="aae32-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="aae32-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aae32-137">NOTES</span></span>

## <span data-ttu-id="aae32-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aae32-138">RELATED LINKS</span></span>

[<span data-ttu-id="aae32-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="aae32-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="aae32-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="aae32-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="aae32-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="aae32-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)