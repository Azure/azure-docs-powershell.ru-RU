---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 6de9fecc4b9576f9d69ddc1f963ae537f4422371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568520"
---
# <span data-ttu-id="a4382-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a4382-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="a4382-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4382-102">SYNOPSIS</span></span>
<span data-ttu-id="a4382-103">Восстановление удаленного ключа из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="a4382-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4382-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4382-104">SYNTAX</span></span>

### <span data-ttu-id="a4382-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4382-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4382-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4382-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4382-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4382-107">DESCRIPTION</span></span>
<span data-ttu-id="a4382-108">Командлет **Undo-AzureKeyVaultKeyRemoval** восстановит ранее удаленную клавишу.</span><span class="sxs-lookup"><span data-stu-id="a4382-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="a4382-109">Восстановленный ключ будет активен и может использоваться для всех обычных операций с ключами.</span><span class="sxs-lookup"><span data-stu-id="a4382-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="a4382-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="a4382-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a4382-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4382-111">EXAMPLES</span></span>

### <span data-ttu-id="a4382-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4382-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="a4382-113">Эта команда восстанавливает в активном и рабочем состоянии раздел "MyKey", который был ранее удален.</span><span class="sxs-lookup"><span data-stu-id="a4382-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a4382-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4382-114">PARAMETERS</span></span>

### <span data-ttu-id="a4382-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4382-115">-DefaultProfile</span></span>
<span data-ttu-id="a4382-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a4382-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4382-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4382-117">-InputObject</span></span>
<span data-ttu-id="a4382-118">Удаленный объект Key</span><span class="sxs-lookup"><span data-stu-id="a4382-118">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4382-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4382-119">-Name</span></span>
<span data-ttu-id="a4382-120">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="a4382-120">Key name.</span></span>
<span data-ttu-id="a4382-121">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="a4382-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4382-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a4382-122">-VaultName</span></span>
<span data-ttu-id="a4382-123">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="a4382-123">Vault name.</span></span>
<span data-ttu-id="a4382-124">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="a4382-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4382-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4382-125">-Confirm</span></span>
<span data-ttu-id="a4382-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4382-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4382-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4382-127">-WhatIf</span></span>
<span data-ttu-id="a4382-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4382-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4382-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4382-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4382-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4382-130">CommonParameters</span></span>
<span data-ttu-id="a4382-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4382-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4382-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4382-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4382-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4382-133">INPUTS</span></span>

### <span data-ttu-id="a4382-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a4382-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="a4382-135">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4382-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a4382-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4382-136">OUTPUTS</span></span>

### <span data-ttu-id="a4382-137">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a4382-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="a4382-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4382-138">NOTES</span></span>

## <span data-ttu-id="a4382-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4382-139">RELATED LINKS</span></span>

[<span data-ttu-id="a4382-140">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a4382-140">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="a4382-141">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a4382-141">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="a4382-142">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a4382-142">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

