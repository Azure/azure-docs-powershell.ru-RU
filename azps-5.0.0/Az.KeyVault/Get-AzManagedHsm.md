---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247727"
---
# <span data-ttu-id="d6ece-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d6ece-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="d6ece-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6ece-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ece-103">Получить управляемый HSMs.</span><span class="sxs-lookup"><span data-stu-id="d6ece-103">Get managed HSMs.</span></span>

## <span data-ttu-id="d6ece-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6ece-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ece-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6ece-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ece-106">Командлет **Get-AzManagedHsm** получает сведения об управляемых HSMsх в подписке.</span><span class="sxs-lookup"><span data-stu-id="d6ece-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="d6ece-107">Вы можете просмотреть все управляемые экземпляры HSMs в подписке или отфильтровать результаты по группе ресурсов или определенному управляемому HSM.</span><span class="sxs-lookup"><span data-stu-id="d6ece-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="d6ece-108">Обратите внимание на то, что, хотя указание группы ресурсов является необязательным для этого командлета при получении единого управляемого HSM-ключа, для лучшей производительности необходимо сделать это.</span><span class="sxs-lookup"><span data-stu-id="d6ece-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="d6ece-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6ece-109">EXAMPLES</span></span>

### <span data-ttu-id="d6ece-110">Пример 1: получение всех управляемых HSMs в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="d6ece-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d6ece-111">Эта команда получает все управляемые HSMs в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d6ece-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="d6ece-112">Пример 2: получение определенного управляемого HSM</span><span class="sxs-lookup"><span data-stu-id="d6ece-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d6ece-113">Эта команда получает управляемый HSM, именуемый myhsm, в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d6ece-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="d6ece-114">Пример 3: получение управляемых HSMs в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6ece-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d6ece-115">Эта команда получает все управляемые HSMs в группе ресурсов с именем myrg1.</span><span class="sxs-lookup"><span data-stu-id="d6ece-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="d6ece-116">Пример 4: получение управляемых HSMs с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="d6ece-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="d6ece-117">Эта команда получает все управляемые HSMs в подписке, которые начинаются с "myhsm".</span><span class="sxs-lookup"><span data-stu-id="d6ece-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="d6ece-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6ece-118">PARAMETERS</span></span>

### <span data-ttu-id="d6ece-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ece-119">-DefaultProfile</span></span>
<span data-ttu-id="d6ece-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ece-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ece-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6ece-121">-Name</span></span>
<span data-ttu-id="d6ece-122">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="d6ece-122">HSM name.</span></span> <span data-ttu-id="d6ece-123">Командлет создает полное доменное имя (FQDN) для HSM на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="d6ece-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ece-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ece-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6ece-125">Указывает имя группы ресурсов, связанной с запрашиваемым управляемым HSM.</span><span class="sxs-lookup"><span data-stu-id="d6ece-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ece-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="d6ece-126">-Tag</span></span>
<span data-ttu-id="d6ece-127">Задает ключ и необязательное значение указанного тега для фильтрации списка управляемых HSMs.</span><span class="sxs-lookup"><span data-stu-id="d6ece-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="d6ece-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ece-128">CommonParameters</span></span>
<span data-ttu-id="d6ece-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6ece-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ece-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6ece-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ece-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6ece-131">INPUTS</span></span>

### <span data-ttu-id="d6ece-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ece-132">System.String</span></span>

### <span data-ttu-id="d6ece-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d6ece-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d6ece-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6ece-134">OUTPUTS</span></span>

### <span data-ttu-id="d6ece-135">Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d6ece-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="d6ece-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d6ece-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="d6ece-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6ece-137">NOTES</span></span>

## <span data-ttu-id="d6ece-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6ece-138">RELATED LINKS</span></span>

[<span data-ttu-id="d6ece-139">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d6ece-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="d6ece-140">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d6ece-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="d6ece-141">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d6ece-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)