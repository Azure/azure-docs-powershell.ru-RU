---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: d37181ae14b0070cd60adca3f6f56f25eab7fd3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235637"
---
# <span data-ttu-id="e7f79-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e7f79-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="e7f79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7f79-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f79-103">Устанавливает свойства ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="e7f79-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="e7f79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7f79-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7f79-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f79-106">Командлет **Set-AzDiskUpdateKeyEncryptionKey** устанавливает свойства ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="e7f79-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="e7f79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7f79-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f79-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7f79-108">Example 1</span></span>
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

<span data-ttu-id="e7f79-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e7f79-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e7f79-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="e7f79-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e7f79-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="e7f79-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="e7f79-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e7f79-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e7f79-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7f79-113">PARAMETERS</span></span>

### <span data-ttu-id="e7f79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f79-114">-DefaultProfile</span></span>
<span data-ttu-id="e7f79-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f79-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f79-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e7f79-116">-DiskUpdate</span></span>
<span data-ttu-id="e7f79-117">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="e7f79-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="e7f79-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="e7f79-118">-KeyUrl</span></span>
<span data-ttu-id="e7f79-119">Задает URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="e7f79-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="e7f79-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e7f79-120">-SourceVaultId</span></span>
<span data-ttu-id="e7f79-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="e7f79-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="e7f79-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7f79-122">-Confirm</span></span>
<span data-ttu-id="e7f79-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7f79-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f79-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f79-124">-WhatIf</span></span>
<span data-ttu-id="e7f79-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7f79-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7f79-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7f79-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f79-127">CommonParameters</span></span>
<span data-ttu-id="e7f79-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7f79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f79-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7f79-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f79-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7f79-130">INPUTS</span></span>

### <span data-ttu-id="e7f79-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e7f79-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="e7f79-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7f79-132">System.String</span></span>

## <span data-ttu-id="e7f79-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7f79-133">OUTPUTS</span></span>

### <span data-ttu-id="e7f79-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e7f79-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="e7f79-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7f79-135">NOTES</span></span>

## <span data-ttu-id="e7f79-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7f79-136">RELATED LINKS</span></span>