---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7e5aa5091376b8c80d71bdeb2bbad7bd8d22c3a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409188"
---
# <span data-ttu-id="149c3-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="149c3-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="149c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="149c3-102">SYNOPSIS</span></span>
<span data-ttu-id="149c3-103">Полное резервное копирование управляемой системы HSM.</span><span class="sxs-lookup"><span data-stu-id="149c3-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="149c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="149c3-104">SYNTAX</span></span>

### <span data-ttu-id="149c3-105">InteractiveStorageName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="149c3-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="149c3-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="149c3-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="149c3-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="149c3-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="149c3-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="149c3-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="149c3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="149c3-109">DESCRIPTION</span></span>
<span data-ttu-id="149c3-110">Полностью архивирование управляемой HSM-системы в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="149c3-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="149c3-111">Используется `Restore-AzKeyVault` для восстановления резервной копии.</span><span class="sxs-lookup"><span data-stu-id="149c3-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="149c3-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="149c3-112">EXAMPLES</span></span>

### <span data-ttu-id="149c3-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="149c3-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="149c3-114">Он создает папку (обычно она называется) в контейнере хранилища, сохраняет резервную копию в этой папке и выводит `mhsm-{name}-{timestamp}` URI папки.</span><span class="sxs-lookup"><span data-stu-id="149c3-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="149c3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="149c3-115">PARAMETERS</span></span>

### <span data-ttu-id="149c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149c3-116">-DefaultProfile</span></span>
<span data-ttu-id="149c3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="149c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="149c3-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="149c3-118">-HsmName</span></span>
<span data-ttu-id="149c3-119">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="149c3-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="149c3-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="149c3-120">-HsmObject</span></span>
<span data-ttu-id="149c3-121">Управляемый объект HSM</span><span class="sxs-lookup"><span data-stu-id="149c3-121">Managed HSM object</span></span>

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

### <span data-ttu-id="149c3-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="149c3-122">-SasToken</span></span>
<span data-ttu-id="149c3-123">Маркер подписи общего доступа (SAS) для проверки подлинности учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="149c3-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="149c3-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="149c3-124">-StorageAccountName</span></span>
<span data-ttu-id="149c3-125">Имя учетной записи хранения, в которой будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="149c3-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="149c3-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="149c3-126">-StorageContainerName</span></span>
<span data-ttu-id="149c3-127">Имя контейнера BLOB-приложений, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="149c3-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="149c3-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="149c3-128">-StorageContainerUri</span></span>
<span data-ttu-id="149c3-129">URI контейнера хранилища, в котором будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="149c3-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="149c3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="149c3-130">-Confirm</span></span>
<span data-ttu-id="149c3-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="149c3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="149c3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="149c3-132">-WhatIf</span></span>
<span data-ttu-id="149c3-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="149c3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="149c3-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="149c3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="149c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149c3-135">CommonParameters</span></span>
<span data-ttu-id="149c3-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="149c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149c3-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="149c3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149c3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="149c3-138">INPUTS</span></span>

### <span data-ttu-id="149c3-139">Нет</span><span class="sxs-lookup"><span data-stu-id="149c3-139">None</span></span>

## <span data-ttu-id="149c3-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="149c3-140">OUTPUTS</span></span>

### <span data-ttu-id="149c3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="149c3-141">System.String</span></span>

## <span data-ttu-id="149c3-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="149c3-142">NOTES</span></span>

## <span data-ttu-id="149c3-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="149c3-143">RELATED LINKS</span></span>