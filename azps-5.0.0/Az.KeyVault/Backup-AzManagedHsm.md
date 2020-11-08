---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245320"
---
# <span data-ttu-id="b6b2d-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="b6b2d-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="b6b2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b2d-103">Полностью архивировать управляемый HSM-объект.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="b6b2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6b2d-104">SYNTAX</span></span>

### <span data-ttu-id="b6b2d-105">InteractiveStorageName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6b2d-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b2d-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="b6b2d-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b2d-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="b6b2d-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b2d-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="b6b2d-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b2d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6b2d-109">DESCRIPTION</span></span>
<span data-ttu-id="b6b2d-110">Полностью создайте резервную копию управляемого HSM-устройства для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="b6b2d-111">Используйте `Restore-AzManagedHsm` для восстановления резервной копии.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="b6b2d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6b2d-112">EXAMPLES</span></span>

### <span data-ttu-id="b6b2d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6b2d-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="b6b2d-114">Командлет создаст в контейнере хранилища папку (обычно именуемую `mhsm-{name}-{timestamp}` ), сохраните ее в этой папке и выводите URI для папки.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="b6b2d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6b2d-115">PARAMETERS</span></span>

### <span data-ttu-id="b6b2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b2d-116">-DefaultProfile</span></span>
<span data-ttu-id="b6b2d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b2d-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="b6b2d-118">-HsmObject</span></span>
<span data-ttu-id="b6b2d-119">Управляемый объект HSM</span><span class="sxs-lookup"><span data-stu-id="b6b2d-119">Managed HSM object</span></span>

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

### <span data-ttu-id="b6b2d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6b2d-120">-Name</span></span>
<span data-ttu-id="b6b2d-121">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="b6b2d-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="b6b2d-122">-SasToken</span></span>
<span data-ttu-id="b6b2d-123">Маркер общего доступа к подписи (SAS) для проверки подлинности учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="b6b2d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b6b2d-124">-StorageAccountName</span></span>
<span data-ttu-id="b6b2d-125">Имя учетной записи хранилища, в которой будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="b6b2d-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="b6b2d-126">-StorageContainerName</span></span>
<span data-ttu-id="b6b2d-127">Имя контейнера BLOB-объектов, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="b6b2d-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="b6b2d-128">-StorageContainerUri</span></span>
<span data-ttu-id="b6b2d-129">Универсальный код ресурса (URI) контейнера хранилища, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="b6b2d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6b2d-130">-Confirm</span></span>
<span data-ttu-id="b6b2d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b2d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b2d-132">-WhatIf</span></span>
<span data-ttu-id="b6b2d-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b2d-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b2d-135">CommonParameters</span></span>
<span data-ttu-id="b6b2d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6b2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b2d-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6b2d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b2d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6b2d-138">INPUTS</span></span>

### <span data-ttu-id="b6b2d-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="b6b2d-139">None</span></span>

## <span data-ttu-id="b6b2d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6b2d-140">OUTPUTS</span></span>

### <span data-ttu-id="b6b2d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b6b2d-141">System.String</span></span>

## <span data-ttu-id="b6b2d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6b2d-142">NOTES</span></span>

## <span data-ttu-id="b6b2d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6b2d-143">RELATED LINKS</span></span>
