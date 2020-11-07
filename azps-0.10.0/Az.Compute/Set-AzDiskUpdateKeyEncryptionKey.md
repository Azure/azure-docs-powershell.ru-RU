---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: b1fe2674360ffec8b2f2c570d47aef3daad78e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911368"
---
# <span data-ttu-id="62955-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="62955-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="62955-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62955-102">SYNOPSIS</span></span>
<span data-ttu-id="62955-103">Устанавливает свойства ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="62955-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="62955-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62955-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62955-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62955-105">DESCRIPTION</span></span>
<span data-ttu-id="62955-106">Командлет **Set-AzDiskUpdateKeyEncryptionKey** устанавливает свойства ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="62955-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="62955-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62955-107">EXAMPLES</span></span>

### <span data-ttu-id="62955-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62955-108">Example 1</span></span>
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

<span data-ttu-id="62955-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="62955-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="62955-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="62955-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="62955-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="62955-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="62955-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="62955-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="62955-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62955-113">PARAMETERS</span></span>

### <span data-ttu-id="62955-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62955-114">-DefaultProfile</span></span>
<span data-ttu-id="62955-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62955-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62955-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="62955-116">-DiskUpdate</span></span>
<span data-ttu-id="62955-117">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="62955-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="62955-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="62955-118">-KeyUrl</span></span>
<span data-ttu-id="62955-119">Specifes URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="62955-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="62955-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="62955-120">-SourceVaultId</span></span>
<span data-ttu-id="62955-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="62955-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="62955-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62955-122">-Confirm</span></span>
<span data-ttu-id="62955-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62955-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62955-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62955-124">-WhatIf</span></span>
<span data-ttu-id="62955-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62955-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62955-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62955-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62955-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62955-127">CommonParameters</span></span>
<span data-ttu-id="62955-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62955-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62955-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62955-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62955-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62955-130">INPUTS</span></span>

### <span data-ttu-id="62955-131">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="62955-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="62955-132">System. String</span><span class="sxs-lookup"><span data-stu-id="62955-132">System.String</span></span>

## <span data-ttu-id="62955-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62955-133">OUTPUTS</span></span>

### <span data-ttu-id="62955-134">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="62955-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="62955-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="62955-135">NOTES</span></span>

## <span data-ttu-id="62955-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62955-136">RELATED LINKS</span></span>

