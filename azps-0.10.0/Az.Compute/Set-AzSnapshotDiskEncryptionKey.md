---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: d6a1284bc92b9479a9ec2a87225bffa56916e4dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911371"
---
# <span data-ttu-id="f7325-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f7325-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="f7325-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7325-102">SYNOPSIS</span></span>
<span data-ttu-id="f7325-103">Задает свойства ключа шифрования диска для объекта-снимка.</span><span class="sxs-lookup"><span data-stu-id="f7325-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="f7325-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7325-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7325-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7325-105">DESCRIPTION</span></span>
<span data-ttu-id="f7325-106">Командлет **Set-AzSnapshotDiskEncryptionKey** задает свойства ключа шифрования диска для объекта-снимка.</span><span class="sxs-lookup"><span data-stu-id="f7325-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="f7325-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7325-107">EXAMPLES</span></span>

### <span data-ttu-id="f7325-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7325-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="f7325-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7325-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="f7325-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="f7325-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f7325-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="f7325-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="f7325-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f7325-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f7325-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7325-113">PARAMETERS</span></span>

### <span data-ttu-id="f7325-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7325-114">-DefaultProfile</span></span>
<span data-ttu-id="f7325-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7325-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7325-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="f7325-116">-SecretUrl</span></span>
<span data-ttu-id="f7325-117">Задает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f7325-117">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7325-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="f7325-118">-Snapshot</span></span>
<span data-ttu-id="f7325-119">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="f7325-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7325-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f7325-120">-SourceVaultId</span></span>
<span data-ttu-id="f7325-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f7325-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7325-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7325-122">-Confirm</span></span>
<span data-ttu-id="f7325-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7325-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7325-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7325-124">-WhatIf</span></span>
<span data-ttu-id="f7325-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7325-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7325-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7325-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7325-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7325-127">CommonParameters</span></span>
<span data-ttu-id="f7325-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7325-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7325-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7325-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7325-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7325-130">INPUTS</span></span>

### <span data-ttu-id="f7325-131">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="f7325-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="f7325-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f7325-132">System.String</span></span>

## <span data-ttu-id="f7325-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7325-133">OUTPUTS</span></span>

### <span data-ttu-id="f7325-134">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="f7325-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="f7325-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7325-135">NOTES</span></span>

## <span data-ttu-id="f7325-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7325-136">RELATED LINKS</span></span>

