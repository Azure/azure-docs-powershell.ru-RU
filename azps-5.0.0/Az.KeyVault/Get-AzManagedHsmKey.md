---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245308"
---
# <span data-ttu-id="5bac5-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="5bac5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bac5-102">SYNOPSIS</span></span>
<span data-ttu-id="5bac5-103">Получает управляемые ключи HSM.</span><span class="sxs-lookup"><span data-stu-id="5bac5-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="5bac5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bac5-104">SYNTAX</span></span>

### <span data-ttu-id="5bac5-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5bac5-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="5bac5-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="5bac5-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="5bac5-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="5bac5-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="5bac5-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="5bac5-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="5bac5-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bac5-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="5bac5-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bac5-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bac5-114">DESCRIPTION</span></span>
<span data-ttu-id="5bac5-115">Командлет **Get-AzManagedHsmKey** получает ключи HSM, управляемые службой Azure.</span><span class="sxs-lookup"><span data-stu-id="5bac5-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="5bac5-116">Этот командлет получает определенный **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** или список всех объектов **KeyBundle** в управляемом HSM или версии.</span><span class="sxs-lookup"><span data-stu-id="5bac5-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="5bac5-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bac5-117">EXAMPLES</span></span>

### <span data-ttu-id="5bac5-118">Пример 1: получение всех ключей в управляемом HSM</span><span class="sxs-lookup"><span data-stu-id="5bac5-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="5bac5-119">Имя хранилища/HSM: testmhsm Name: testkey001 Version: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled: true Expires: not before: Created: 10/14/2020 3:39:16-Обновлено: 10/14/2020 3:39:16 по уровню восстановления: подлежащие восстановлению теги, которые могут быть очищены:</span><span class="sxs-lookup"><span data-stu-id="5bac5-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="5bac5-120">Имя хранилища/HSM: testmhsm Name: testkey002 Version: ID: Enabled: false: 10/14/2020 8:13:33:10/14/2020 8:14:01 (-а): https://testmhsm.managedhsm.azure.net:443/keys/testkey002 10/14/2022 8:13:29-Дата обновления: 10/14/2020 8:14:01 — более ранние версии: с возможностью восстановления и удаления тегов: имя значения степень серьезности</span><span class="sxs-lookup"><span data-stu-id="5bac5-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="5bac5-121">Эта команда получает все ключи в управляемом HSM, именуемом testmhsm.</span><span class="sxs-lookup"><span data-stu-id="5bac5-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="5bac5-122">Пример 2: получение текущей версии ключа</span><span class="sxs-lookup"><span data-stu-id="5bac5-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="5bac5-123">Эта команда получает текущую версию ключа с именем testkey001 в управляемом HSM, именуемом testmhsm.</span><span class="sxs-lookup"><span data-stu-id="5bac5-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="5bac5-124">Примечание: имя HSM может быть получено $hsm. VaultName</span><span class="sxs-lookup"><span data-stu-id="5bac5-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="5bac5-125">Пример 3: получение всех версий ключа</span><span class="sxs-lookup"><span data-stu-id="5bac5-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="5bac5-126">Эта команда возвращает все версии Key с именем testkey001 в управляемом HSM, именуемом testmhsm.</span><span class="sxs-lookup"><span data-stu-id="5bac5-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="5bac5-127">Пример 4: получение определенной версии ключа</span><span class="sxs-lookup"><span data-stu-id="5bac5-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="5bac5-128">Эта команда возвращает определенную версию ключа с именем TestKey в управляемом HSM, именуемом testmhsm.</span><span class="sxs-lookup"><span data-stu-id="5bac5-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="5bac5-129">После выполнения этой команды вы можете просматривать различные свойства ключа, перемещаясь по объекту $Key.</span><span class="sxs-lookup"><span data-stu-id="5bac5-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="5bac5-130">Пример 5: получение всех ключей, которые были удалены, но не очищены для этого управляемого HSM</span><span class="sxs-lookup"><span data-stu-id="5bac5-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="5bac5-131">Эта команда возвращает все ключи, которые были ранее удалены, но не очищены, в управляемом HSM, именуемом testmhsm.</span><span class="sxs-lookup"><span data-stu-id="5bac5-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="5bac5-132">Пример 6: получение ключа TestKey, который был удален, но не очищен для этого управляемого HSM</span><span class="sxs-lookup"><span data-stu-id="5bac5-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="5bac5-133">Эта команда возвращает клавишу TestKey, которая была ранее удалена, но не очищена, в управляемом HSM, именуемом testmhsm.</span><span class="sxs-lookup"><span data-stu-id="5bac5-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="5bac5-134">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного ключа.</span><span class="sxs-lookup"><span data-stu-id="5bac5-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="5bac5-135">Пример 7: получение всех ключей в управляемом HSM с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="5bac5-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="5bac5-136">Эта команда получает все ключи в управляемом HSM-процессе с именем testmhsm, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="5bac5-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="5bac5-137">Пример 8: Загрузка открытого ключа в виде PEM-файла</span><span class="sxs-lookup"><span data-stu-id="5bac5-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="5bac5-138">Открытый ключ ключа RSA можно загрузить, указав `-OutFile` параметр.</span><span class="sxs-lookup"><span data-stu-id="5bac5-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="5bac5-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bac5-139">PARAMETERS</span></span>

### <span data-ttu-id="5bac5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bac5-140">-DefaultProfile</span></span>
<span data-ttu-id="5bac5-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bac5-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bac5-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="5bac5-142">-HsmName</span></span>
<span data-ttu-id="5bac5-143">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="5bac5-143">HSM name.</span></span> <span data-ttu-id="5bac5-144">Командлет создает полное доменное имя управляемого HSM-файла на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="5bac5-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bac5-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="5bac5-145">-IncludeVersions</span></span>
<span data-ttu-id="5bac5-146">Указывает, следует ли включать в выходные данные версии ключа.</span><span class="sxs-lookup"><span data-stu-id="5bac5-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bac5-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bac5-147">-InputObject</span></span>
<span data-ttu-id="5bac5-148">Объект HSM.</span><span class="sxs-lookup"><span data-stu-id="5bac5-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bac5-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5bac5-149">-InRemovedState</span></span>
<span data-ttu-id="5bac5-150">Указывает, нужно ли отображать ранее удаленные разделы в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5bac5-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bac5-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5bac5-151">-Name</span></span>
<span data-ttu-id="5bac5-152">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="5bac5-152">Key name.</span></span>
<span data-ttu-id="5bac5-153">Командлет конструирует полное доменное имя ключа из управляемого имени HSM, в настоящее время выбранной среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="5bac5-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bac5-154">-Файл</span><span class="sxs-lookup"><span data-stu-id="5bac5-154">-OutFile</span></span>
<span data-ttu-id="5bac5-155">Указывает выходной файл, для которого этот командлет сохраняет ключ.</span><span class="sxs-lookup"><span data-stu-id="5bac5-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="5bac5-156">Открытый ключ по умолчанию сохраняется в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="5bac5-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="5bac5-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bac5-157">-ResourceId</span></span>
<span data-ttu-id="5bac5-158">Идентификатор ресурса HSM.</span><span class="sxs-lookup"><span data-stu-id="5bac5-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bac5-159">-Version</span><span class="sxs-lookup"><span data-stu-id="5bac5-159">-Version</span></span>
<span data-ttu-id="5bac5-160">Версия ключа.</span><span class="sxs-lookup"><span data-stu-id="5bac5-160">Key version.</span></span>
<span data-ttu-id="5bac5-161">Командлет создает полное доменное имя ключа из управляемого имени HSM, в выбранной среде, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="5bac5-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bac5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bac5-162">CommonParameters</span></span>
<span data-ttu-id="5bac5-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bac5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bac5-164">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bac5-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bac5-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bac5-165">INPUTS</span></span>

### <span data-ttu-id="5bac5-166">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5bac5-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="5bac5-167">System. String</span><span class="sxs-lookup"><span data-stu-id="5bac5-167">System.String</span></span>

## <span data-ttu-id="5bac5-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bac5-168">OUTPUTS</span></span>

### <span data-ttu-id="5bac5-169">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5bac5-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="5bac5-170">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="5bac5-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5bac5-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="5bac5-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="5bac5-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bac5-173">NOTES</span></span>

## <span data-ttu-id="5bac5-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bac5-174">RELATED LINKS</span></span>

[<span data-ttu-id="5bac5-175">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="5bac5-176">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="5bac5-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="5bac5-178">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="5bac5-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="5bac5-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="5bac5-180">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="5bac5-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)