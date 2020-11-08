---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250206"
---
# <span data-ttu-id="ff97d-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ff97d-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="ff97d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff97d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff97d-103">Полностью восстанавливает управляемый HSM из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ff97d-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="ff97d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff97d-104">SYNTAX</span></span>

### <span data-ttu-id="ff97d-105">InteractiveStorageName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff97d-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff97d-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="ff97d-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff97d-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="ff97d-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff97d-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="ff97d-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff97d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff97d-109">DESCRIPTION</span></span>
<span data-ttu-id="ff97d-110">Полностью восстанавливает управляемый HSM из резервной копии, хранящейся в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ff97d-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="ff97d-111">Используется `Backup-AzManagedHsm` для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ff97d-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="ff97d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff97d-112">EXAMPLES</span></span>

### <span data-ttu-id="ff97d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff97d-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="ff97d-114">В примере восстанавливается резервная копия, хранящаяся в папке "mhsm-myHsm-2020101308504935" контейнера хранилища "https://{имя_учетной_записи}. BLOB. Core. Windows. NET/{containerName}".</span><span class="sxs-lookup"><span data-stu-id="ff97d-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="ff97d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff97d-115">PARAMETERS</span></span>

### <span data-ttu-id="ff97d-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="ff97d-116">-BackupFolder</span></span>
<span data-ttu-id="ff97d-117">Имя папки резервной копии, например "mhsm- *-2020101309020403". Его также можно вложить, например "резервные копии/mhsm-* -2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="ff97d-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

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

### <span data-ttu-id="ff97d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff97d-118">-DefaultProfile</span></span>
<span data-ttu-id="ff97d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff97d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff97d-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="ff97d-120">-HsmObject</span></span>
<span data-ttu-id="ff97d-121">Управляемый объект HSM</span><span class="sxs-lookup"><span data-stu-id="ff97d-121">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff97d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff97d-122">-Name</span></span>
<span data-ttu-id="ff97d-123">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="ff97d-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff97d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff97d-124">-PassThru</span></span>
<span data-ttu-id="ff97d-125">Возвращает значение "истина" при восстановлении HSM.</span><span class="sxs-lookup"><span data-stu-id="ff97d-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="ff97d-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="ff97d-126">-SasToken</span></span>
<span data-ttu-id="ff97d-127">Маркер общего доступа к подписи (SAS) для проверки подлинности учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ff97d-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="ff97d-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff97d-128">-StorageAccountName</span></span>
<span data-ttu-id="ff97d-129">Имя учетной записи хранилища, в которой будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="ff97d-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ff97d-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="ff97d-130">-StorageContainerName</span></span>
<span data-ttu-id="ff97d-131">Имя контейнера BLOB-объектов, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="ff97d-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ff97d-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="ff97d-132">-StorageContainerUri</span></span>
<span data-ttu-id="ff97d-133">Универсальный код ресурса (URI) контейнера хранилища, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="ff97d-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ff97d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff97d-134">-Confirm</span></span>
<span data-ttu-id="ff97d-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff97d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff97d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff97d-136">-WhatIf</span></span>
<span data-ttu-id="ff97d-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff97d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff97d-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff97d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff97d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff97d-139">CommonParameters</span></span>
<span data-ttu-id="ff97d-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff97d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff97d-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff97d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff97d-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff97d-142">INPUTS</span></span>

### <span data-ttu-id="ff97d-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="ff97d-143">None</span></span>

## <span data-ttu-id="ff97d-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff97d-144">OUTPUTS</span></span>

### <span data-ttu-id="ff97d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff97d-145">System.Boolean</span></span>

## <span data-ttu-id="ff97d-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff97d-146">NOTES</span></span>

## <span data-ttu-id="ff97d-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff97d-147">RELATED LINKS</span></span>
