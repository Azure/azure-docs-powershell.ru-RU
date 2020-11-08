---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 29090d0c59ef5c32dd74b622c2a79d477419c3b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079783"
---
# <span data-ttu-id="01948-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="01948-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="01948-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01948-102">SYNOPSIS</span></span>
<span data-ttu-id="01948-103">Задает ключевые свойства ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="01948-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="01948-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01948-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01948-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01948-105">DESCRIPTION</span></span>
<span data-ttu-id="01948-106">Командлет **Set-AzDiskKeyEncryptionKey** задает свойства ключа шифрования для дискового объекта.</span><span class="sxs-lookup"><span data-stu-id="01948-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="01948-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01948-107">EXAMPLES</span></span>

### <span data-ttu-id="01948-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01948-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskconfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1';
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="01948-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="01948-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="01948-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="01948-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="01948-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="01948-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="01948-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="01948-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="01948-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01948-113">PARAMETERS</span></span>

### <span data-ttu-id="01948-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01948-114">-DefaultProfile</span></span>
<span data-ttu-id="01948-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01948-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01948-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="01948-116">-Disk</span></span>
<span data-ttu-id="01948-117">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="01948-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="01948-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="01948-118">-KeyUrl</span></span>
<span data-ttu-id="01948-119">Задает URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="01948-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="01948-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="01948-120">-SourceVaultId</span></span>
<span data-ttu-id="01948-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="01948-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="01948-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01948-122">-Confirm</span></span>
<span data-ttu-id="01948-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01948-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01948-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01948-124">-WhatIf</span></span>
<span data-ttu-id="01948-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01948-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01948-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01948-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01948-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01948-127">CommonParameters</span></span>
<span data-ttu-id="01948-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01948-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01948-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01948-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01948-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01948-130">INPUTS</span></span>

### <span data-ttu-id="01948-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="01948-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="01948-132">System. String</span><span class="sxs-lookup"><span data-stu-id="01948-132">System.String</span></span>

## <span data-ttu-id="01948-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01948-133">OUTPUTS</span></span>

### <span data-ttu-id="01948-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="01948-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="01948-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="01948-135">NOTES</span></span>

## <span data-ttu-id="01948-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01948-136">RELATED LINKS</span></span>
