---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 8ef1bccc711b96eb4b06c0b1234a426f9752208d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238716"
---
# <span data-ttu-id="bef99-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bef99-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="bef99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bef99-102">SYNOPSIS</span></span>
<span data-ttu-id="bef99-103">Задает свойства ключа шифрования диска для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="bef99-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="bef99-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bef99-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bef99-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bef99-105">DESCRIPTION</span></span>
<span data-ttu-id="bef99-106">Для свойства ключа шифрования диска для объекта диска используется **cmdlet Set-AzDiskDiskEncryptionKey.**</span><span class="sxs-lookup"><span data-stu-id="bef99-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="bef99-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bef99-107">EXAMPLES</span></span>

### <span data-ttu-id="bef99-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bef99-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1'; 
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="bef99-109">Первая команда создает локальный пустой диск с размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bef99-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="bef99-110">Она также задает тип ОС Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="bef99-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="bef99-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="bef99-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="bef99-112">Последняя команда принимает объект диска и создает диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="bef99-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bef99-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bef99-113">PARAMETERS</span></span>

### <span data-ttu-id="bef99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef99-114">-DefaultProfile</span></span>
<span data-ttu-id="bef99-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bef99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bef99-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="bef99-116">-Disk</span></span>
<span data-ttu-id="bef99-117">Определяет объект локального диска.</span><span class="sxs-lookup"><span data-stu-id="bef99-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="bef99-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="bef99-118">-SecretUrl</span></span>
<span data-ttu-id="bef99-119">Указывает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="bef99-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="bef99-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bef99-120">-SourceVaultId</span></span>
<span data-ttu-id="bef99-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="bef99-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="bef99-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bef99-122">-Confirm</span></span>
<span data-ttu-id="bef99-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef99-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bef99-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef99-124">-WhatIf</span></span>
<span data-ttu-id="bef99-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef99-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bef99-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bef99-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bef99-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef99-127">CommonParameters</span></span>
<span data-ttu-id="bef99-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef99-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef99-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bef99-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef99-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bef99-130">INPUTS</span></span>

### <span data-ttu-id="bef99-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDокне</span><span class="sxs-lookup"><span data-stu-id="bef99-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="bef99-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bef99-132">System.String</span></span>

## <span data-ttu-id="bef99-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bef99-133">OUTPUTS</span></span>

### <span data-ttu-id="bef99-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDокне</span><span class="sxs-lookup"><span data-stu-id="bef99-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="bef99-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bef99-135">NOTES</span></span>

## <span data-ttu-id="bef99-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bef99-136">RELATED LINKS</span></span>
