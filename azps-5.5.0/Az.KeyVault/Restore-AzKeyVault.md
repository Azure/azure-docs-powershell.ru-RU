---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243349"
---
# <span data-ttu-id="7fb67-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7fb67-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="7fb67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb67-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb67-103">Полностью восстанавливает управляемый HSM из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="7fb67-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="7fb67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7fb67-104">SYNTAX</span></span>

### <span data-ttu-id="7fb67-105">InteractiveStorageName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fb67-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb67-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="7fb67-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb67-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="7fb67-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb67-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="7fb67-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb67-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb67-109">DESCRIPTION</span></span>
<span data-ttu-id="7fb67-110">Полностью восстанавливает управляемый HSM из резервной копии, храняной в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7fb67-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="7fb67-111">Используется `Backup-AzKeyVault` для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7fb67-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="7fb67-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7fb67-112">EXAMPLES</span></span>

### <span data-ttu-id="7fb67-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7fb67-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="7fb67-114">В этом примере восстанавливается резервная копия, храняная в папке mhsm-myHsm-2020101308504935" контейнера хранилища "https://{accountName}.blob.core.windows.net/{containerName}".</span><span class="sxs-lookup"><span data-stu-id="7fb67-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="7fb67-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fb67-115">PARAMETERS</span></span>

### <span data-ttu-id="7fb67-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="7fb67-116">-BackupFolder</span></span>
<span data-ttu-id="7fb67-117">Имя папки резервной копии, например "mhsm-*-2020101309020403". В нее также можно вложены такие как "резервное копирование/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="7fb67-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb67-118">-DefaultProfile</span></span>
<span data-ttu-id="7fb67-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb67-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7fb67-120">-HsmName</span></span>
<span data-ttu-id="7fb67-121">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="7fb67-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="7fb67-122">-HsmObject</span></span>
<span data-ttu-id="7fb67-123">Управляемый объект HSM</span><span class="sxs-lookup"><span data-stu-id="7fb67-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7fb67-124">-KeyName</span></span>
<span data-ttu-id="7fb67-125">Имя ключа, которое нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="7fb67-125">Key name to restore.</span></span>

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

### <span data-ttu-id="7fb67-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fb67-126">-PassThru</span></span>
<span data-ttu-id="7fb67-127">Возвращается истина при восстановлении HSM.</span><span class="sxs-lookup"><span data-stu-id="7fb67-127">Return true when the HSM is restored.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="7fb67-128">-SasToken</span></span>
<span data-ttu-id="7fb67-129">Маркер подписи общего доступа (SAS) для проверки подлинности учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7fb67-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7fb67-130">-StorageAccountName</span></span>
<span data-ttu-id="7fb67-131">Имя учетной записи хранения, в которой будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="7fb67-131">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="7fb67-132">-StorageContainerName</span></span>
<span data-ttu-id="7fb67-133">Имя контейнера BLOB-приложений, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="7fb67-133">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="7fb67-134">-StorageContainerUri</span></span>
<span data-ttu-id="7fb67-135">URI контейнера хранилища, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="7fb67-135">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fb67-136">-Confirm</span></span>
<span data-ttu-id="7fb67-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb67-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb67-138">-WhatIf</span></span>
<span data-ttu-id="7fb67-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb67-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb67-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7fb67-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb67-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb67-141">CommonParameters</span></span>
<span data-ttu-id="7fb67-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb67-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb67-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fb67-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb67-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fb67-144">INPUTS</span></span>

### <span data-ttu-id="7fb67-145">Нет</span><span class="sxs-lookup"><span data-stu-id="7fb67-145">None</span></span>

## <span data-ttu-id="7fb67-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7fb67-146">OUTPUTS</span></span>

### <span data-ttu-id="7fb67-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7fb67-147">System.Boolean</span></span>

## <span data-ttu-id="7fb67-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7fb67-148">NOTES</span></span>

## <span data-ttu-id="7fb67-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fb67-149">RELATED LINKS</span></span>
