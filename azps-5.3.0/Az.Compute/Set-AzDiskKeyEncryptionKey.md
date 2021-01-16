---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 6f2037b638b8fd055ef79ca6a8502a17bd5f7911
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509066"
---
# <span data-ttu-id="700dd-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="700dd-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="700dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="700dd-102">SYNOPSIS</span></span>
<span data-ttu-id="700dd-103">Задает свойства ключа шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="700dd-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="700dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="700dd-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="700dd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="700dd-105">DESCRIPTION</span></span>
<span data-ttu-id="700dd-106">Для объекта диска свойства ключа шифрования задаются стебликом **Set-AzDiskKeyEncryptionKey.**</span><span class="sxs-lookup"><span data-stu-id="700dd-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="700dd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="700dd-107">EXAMPLES</span></span>

### <span data-ttu-id="700dd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="700dd-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskconfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1';
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="700dd-109">Первая команда создает локальный пустой диск с размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="700dd-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="700dd-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="700dd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="700dd-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="700dd-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="700dd-112">Последняя команда принимает объект диска и создает диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="700dd-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="700dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="700dd-113">PARAMETERS</span></span>

### <span data-ttu-id="700dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="700dd-114">-DefaultProfile</span></span>
<span data-ttu-id="700dd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="700dd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="700dd-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="700dd-116">-Disk</span></span>
<span data-ttu-id="700dd-117">Определяет объект локального диска.</span><span class="sxs-lookup"><span data-stu-id="700dd-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="700dd-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="700dd-118">-KeyUrl</span></span>
<span data-ttu-id="700dd-119">Указывает URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="700dd-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="700dd-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="700dd-120">-SourceVaultId</span></span>
<span data-ttu-id="700dd-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="700dd-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="700dd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="700dd-122">-Confirm</span></span>
<span data-ttu-id="700dd-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="700dd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="700dd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="700dd-124">-WhatIf</span></span>
<span data-ttu-id="700dd-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="700dd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="700dd-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="700dd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="700dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="700dd-127">CommonParameters</span></span>
<span data-ttu-id="700dd-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="700dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="700dd-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="700dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="700dd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="700dd-130">INPUTS</span></span>

### <span data-ttu-id="700dd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="700dd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="700dd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="700dd-132">System.String</span></span>

## <span data-ttu-id="700dd-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="700dd-133">OUTPUTS</span></span>

### <span data-ttu-id="700dd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="700dd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="700dd-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="700dd-135">NOTES</span></span>

## <span data-ttu-id="700dd-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="700dd-136">RELATED LINKS</span></span>