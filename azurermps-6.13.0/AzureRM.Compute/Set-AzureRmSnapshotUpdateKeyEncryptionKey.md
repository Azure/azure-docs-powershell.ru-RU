---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: fbd62d704bcbb3a73910d1c19db3698a09c6a90f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734676"
---
# <span data-ttu-id="b89ad-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b89ad-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="b89ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b89ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b89ad-103">Устанавливает свойства ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b89ad-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b89ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b89ad-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b89ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b89ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b89ad-106">Командлет **Set-AzureRmSnapshotUpdateKeyEncryptionKey** устанавливает свойства ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b89ad-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="b89ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b89ad-107">EXAMPLES</span></span>

### <span data-ttu-id="b89ad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b89ad-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="b89ad-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b89ad-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b89ad-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="b89ad-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b89ad-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b89ad-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b89ad-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b89ad-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b89ad-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b89ad-113">PARAMETERS</span></span>

### <span data-ttu-id="b89ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89ad-114">-DefaultProfile</span></span>
<span data-ttu-id="b89ad-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b89ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b89ad-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="b89ad-116">-KeyUrl</span></span>
<span data-ttu-id="b89ad-117">Specifes URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="b89ad-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="b89ad-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b89ad-118">-SnapshotUpdate</span></span>
<span data-ttu-id="b89ad-119">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b89ad-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89ad-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b89ad-120">-SourceVaultId</span></span>
<span data-ttu-id="b89ad-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="b89ad-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="b89ad-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b89ad-122">-Confirm</span></span>
<span data-ttu-id="b89ad-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b89ad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b89ad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b89ad-124">-WhatIf</span></span>
<span data-ttu-id="b89ad-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b89ad-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b89ad-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b89ad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b89ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89ad-127">CommonParameters</span></span>
<span data-ttu-id="b89ad-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b89ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89ad-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89ad-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b89ad-130">INPUTS</span></span>

### <span data-ttu-id="b89ad-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b89ad-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="b89ad-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b89ad-132">System.String</span></span>

## <span data-ttu-id="b89ad-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b89ad-133">OUTPUTS</span></span>

### <span data-ttu-id="b89ad-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b89ad-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="b89ad-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b89ad-135">NOTES</span></span>

## <span data-ttu-id="b89ad-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b89ad-136">RELATED LINKS</span></span>
