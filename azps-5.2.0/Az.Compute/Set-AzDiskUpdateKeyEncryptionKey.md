---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 73c765d35238d960a95b86c90ad2ff7f2cd5db11
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396932"
---
# <span data-ttu-id="01bb2-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="01bb2-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="01bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="01bb2-103">Задает свойства ключа шифрования ключа для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="01bb2-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="01bb2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01bb2-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01bb2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="01bb2-106">Cmdlet **Set-AzDiskUpdateKeyEncryptionKey** задает свойства ключа шифрования ключа для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="01bb2-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="01bb2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="01bb2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01bb2-108">Example 1</span></span>
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

<span data-ttu-id="01bb2-109">Первая команда создает объект обновления локального пустого диска с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="01bb2-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="01bb2-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="01bb2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="01bb2-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="01bb2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="01bb2-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="01bb2-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="01bb2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01bb2-113">PARAMETERS</span></span>

### <span data-ttu-id="01bb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bb2-114">-DefaultProfile</span></span>
<span data-ttu-id="01bb2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01bb2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01bb2-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="01bb2-116">-DiskUpdate</span></span>
<span data-ttu-id="01bb2-117">Определяет объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="01bb2-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="01bb2-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="01bb2-118">-KeyUrl</span></span>
<span data-ttu-id="01bb2-119">Указывает URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="01bb2-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="01bb2-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="01bb2-120">-SourceVaultId</span></span>
<span data-ttu-id="01bb2-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="01bb2-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="01bb2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01bb2-122">-Confirm</span></span>
<span data-ttu-id="01bb2-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="01bb2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01bb2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01bb2-124">-WhatIf</span></span>
<span data-ttu-id="01bb2-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01bb2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01bb2-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="01bb2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01bb2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bb2-127">CommonParameters</span></span>
<span data-ttu-id="01bb2-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01bb2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bb2-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01bb2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bb2-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01bb2-130">INPUTS</span></span>

### <span data-ttu-id="01bb2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="01bb2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="01bb2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="01bb2-132">System.String</span></span>

## <span data-ttu-id="01bb2-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01bb2-133">OUTPUTS</span></span>

### <span data-ttu-id="01bb2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="01bb2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="01bb2-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01bb2-135">NOTES</span></span>

## <span data-ttu-id="01bb2-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01bb2-136">RELATED LINKS</span></span>
