---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 51a501e2b01ef044685f4172d42bad5342cb462c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244064"
---
# <span data-ttu-id="453fe-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="453fe-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="453fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="453fe-102">SYNOPSIS</span></span>
<span data-ttu-id="453fe-103">Задает свойства ключа шифрования диска для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="453fe-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="453fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="453fe-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="453fe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="453fe-105">DESCRIPTION</span></span>
<span data-ttu-id="453fe-106">Cmdlet **Set-AzDiskUpdateDiskEncryptionKey** задает свойства ключа шифрования диска для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="453fe-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="453fe-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="453fe-107">EXAMPLES</span></span>

### <span data-ttu-id="453fe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="453fe-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="453fe-109">Первая команда создает объект обновления локального пустого диска с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="453fe-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="453fe-110">Она также задает тип ОС Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="453fe-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="453fe-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="453fe-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="453fe-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="453fe-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="453fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="453fe-113">PARAMETERS</span></span>

### <span data-ttu-id="453fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453fe-114">-DefaultProfile</span></span>
<span data-ttu-id="453fe-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="453fe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="453fe-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="453fe-116">-DiskUpdate</span></span>
<span data-ttu-id="453fe-117">Определяет объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="453fe-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="453fe-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="453fe-118">-SecretUrl</span></span>
<span data-ttu-id="453fe-119">Указывает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="453fe-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="453fe-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="453fe-120">-SourceVaultId</span></span>
<span data-ttu-id="453fe-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="453fe-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="453fe-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="453fe-122">-Confirm</span></span>
<span data-ttu-id="453fe-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="453fe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453fe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453fe-124">-WhatIf</span></span>
<span data-ttu-id="453fe-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="453fe-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="453fe-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="453fe-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453fe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453fe-127">CommonParameters</span></span>
<span data-ttu-id="453fe-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="453fe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453fe-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="453fe-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453fe-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="453fe-130">INPUTS</span></span>

### <span data-ttu-id="453fe-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="453fe-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="453fe-132">System.String</span><span class="sxs-lookup"><span data-stu-id="453fe-132">System.String</span></span>

## <span data-ttu-id="453fe-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="453fe-133">OUTPUTS</span></span>

### <span data-ttu-id="453fe-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="453fe-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="453fe-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="453fe-135">NOTES</span></span>

## <span data-ttu-id="453fe-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="453fe-136">RELATED LINKS</span></span>
