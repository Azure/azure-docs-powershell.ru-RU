---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 0f55058bc3419805bf7270e4d03c75db2208669e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911373"
---
# <span data-ttu-id="e0dfd-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e0dfd-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="e0dfd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dfd-103">Задает параметры ключа шифрования диска в объекте обновления диска.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-103">Sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="e0dfd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0dfd-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0dfd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="e0dfd-106">Командлет **Set-AzDiskUpdateDiskEncryptionKey** задает свойства ключа шифрования диска в объекте обновления диска.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="e0dfd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="e0dfd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0dfd-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="e0dfd-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e0dfd-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e0dfd-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="e0dfd-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e0dfd-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e0dfd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0dfd-113">PARAMETERS</span></span>

### <span data-ttu-id="e0dfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dfd-114">-DefaultProfile</span></span>
<span data-ttu-id="e0dfd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0dfd-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e0dfd-116">-DiskUpdate</span></span>
<span data-ttu-id="e0dfd-117">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-117">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0dfd-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="e0dfd-118">-SecretUrl</span></span>
<span data-ttu-id="e0dfd-119">Задает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="e0dfd-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e0dfd-120">-SourceVaultId</span></span>
<span data-ttu-id="e0dfd-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="e0dfd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0dfd-122">-Confirm</span></span>
<span data-ttu-id="e0dfd-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0dfd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0dfd-124">-WhatIf</span></span>
<span data-ttu-id="e0dfd-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0dfd-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0dfd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dfd-127">CommonParameters</span></span>
<span data-ttu-id="e0dfd-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0dfd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dfd-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0dfd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dfd-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0dfd-130">INPUTS</span></span>

### <span data-ttu-id="e0dfd-131">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e0dfd-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="e0dfd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e0dfd-132">System.String</span></span>

## <span data-ttu-id="e0dfd-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0dfd-133">OUTPUTS</span></span>

### <span data-ttu-id="e0dfd-134">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e0dfd-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="e0dfd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0dfd-135">NOTES</span></span>

## <span data-ttu-id="e0dfd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0dfd-136">RELATED LINKS</span></span>

