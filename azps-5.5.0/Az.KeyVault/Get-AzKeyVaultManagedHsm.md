---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214513"
---
# <span data-ttu-id="f8b80-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f8b80-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="f8b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b80-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b80-103">Получите управляемые HSMs.</span><span class="sxs-lookup"><span data-stu-id="f8b80-103">Get managed HSMs.</span></span>

## <span data-ttu-id="f8b80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8b80-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b80-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8b80-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b80-106">**Cmdlet Get-AzKeyVaultManagedHsm** получает сведения об управляемых HSMs в подписке.</span><span class="sxs-lookup"><span data-stu-id="f8b80-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="f8b80-107">Вы можете просмотреть все управляемые HSMs-экземпляры в подписке или отфильтровать результаты по группе ресурсов или определенной управляемой службе управления HSM.</span><span class="sxs-lookup"><span data-stu-id="f8b80-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="f8b80-108">Имейте в виду, что хотя при работе с одним управляемым HSM-решением указать группу ресурсов необязательно, это следует сделать для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="f8b80-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="f8b80-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8b80-109">EXAMPLES</span></span>

### <span data-ttu-id="f8b80-110">Пример 1. Все управляемые HSMs в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="f8b80-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="f8b80-111">Эта команда получает все управляемые HSMs в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f8b80-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="f8b80-112">Пример 2. Получить Управлили HSM</span><span class="sxs-lookup"><span data-stu-id="f8b80-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="f8b80-113">Эта команда получает управляемый HSM-службу с именем myhsm в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f8b80-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="f8b80-114">Пример 3. Управление HSMs в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f8b80-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="f8b80-115">Эта команда получает все управляемые HSMs в группе ресурсов myrg1.</span><span class="sxs-lookup"><span data-stu-id="f8b80-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="f8b80-116">Пример 4. Управление HSMs с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="f8b80-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="f8b80-117">Эта команда получает все управляемые HSMs в подписке, которая начинается с "myhsm".</span><span class="sxs-lookup"><span data-stu-id="f8b80-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="f8b80-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8b80-118">PARAMETERS</span></span>

### <span data-ttu-id="f8b80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b80-119">-DefaultProfile</span></span>
<span data-ttu-id="f8b80-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b80-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b80-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8b80-121">-Name</span></span>
<span data-ttu-id="f8b80-122">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="f8b80-122">HSM name.</span></span> <span data-ttu-id="f8b80-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="f8b80-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f8b80-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b80-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8b80-125">Имя группы ресурсов, связанной с запрашиваемой управляемой службой управления ресурсами.</span><span class="sxs-lookup"><span data-stu-id="f8b80-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

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

### <span data-ttu-id="f8b80-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8b80-126">-Tag</span></span>
<span data-ttu-id="f8b80-127">Указывает ключ и необязательное значение указанного тега для фильтрации списка управляемых сообщений HSMs по.</span><span class="sxs-lookup"><span data-stu-id="f8b80-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="f8b80-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b80-128">CommonParameters</span></span>
<span data-ttu-id="f8b80-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b80-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b80-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b80-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b80-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8b80-131">INPUTS</span></span>

### <span data-ttu-id="f8b80-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f8b80-132">System.String</span></span>

### <span data-ttu-id="f8b80-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f8b80-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f8b80-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8b80-134">OUTPUTS</span></span>

### <span data-ttu-id="f8b80-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f8b80-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="f8b80-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f8b80-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="f8b80-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8b80-137">NOTES</span></span>

## <span data-ttu-id="f8b80-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8b80-138">RELATED LINKS</span></span>

[<span data-ttu-id="f8b80-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f8b80-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="f8b80-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f8b80-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="f8b80-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f8b80-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)