---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 5a976481abb446e4e78305abf3beee11da98fbde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731251"
---
# <span data-ttu-id="74b1a-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="74b1a-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="74b1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="74b1a-103">Задает свойства ключа шифрования диска для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="74b1a-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="74b1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74b1a-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74b1a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="74b1a-106">Командлет **Set-AzDiskUpdateDiskEncryptionKey** задает свойства ключа шифрования дисков в объекте обновления диска.</span><span class="sxs-lookup"><span data-stu-id="74b1a-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="74b1a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="74b1a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74b1a-108">Example 1</span></span>
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

<span data-ttu-id="74b1a-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="74b1a-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="74b1a-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="74b1a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="74b1a-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="74b1a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="74b1a-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="74b1a-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="74b1a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74b1a-113">PARAMETERS</span></span>

### <span data-ttu-id="74b1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b1a-114">-DefaultProfile</span></span>
<span data-ttu-id="74b1a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74b1a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b1a-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="74b1a-116">-DiskUpdate</span></span>
<span data-ttu-id="74b1a-117">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="74b1a-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74b1a-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="74b1a-118">-SecretUrl</span></span>
<span data-ttu-id="74b1a-119">Задает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="74b1a-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="74b1a-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="74b1a-120">-SourceVaultId</span></span>
<span data-ttu-id="74b1a-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="74b1a-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="74b1a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74b1a-122">-Confirm</span></span>
<span data-ttu-id="74b1a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74b1a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b1a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b1a-124">-WhatIf</span></span>
<span data-ttu-id="74b1a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74b1a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74b1a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74b1a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b1a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b1a-127">CommonParameters</span></span>
<span data-ttu-id="74b1a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74b1a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b1a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b1a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b1a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74b1a-130">INPUTS</span></span>

### <span data-ttu-id="74b1a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="74b1a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="74b1a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="74b1a-132">System.String</span></span>

## <span data-ttu-id="74b1a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74b1a-133">OUTPUTS</span></span>

### <span data-ttu-id="74b1a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="74b1a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="74b1a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="74b1a-135">NOTES</span></span>

## <span data-ttu-id="74b1a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74b1a-136">RELATED LINKS</span></span>
