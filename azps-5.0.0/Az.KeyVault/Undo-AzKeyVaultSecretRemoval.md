---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245281"
---
# <span data-ttu-id="d281c-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="d281c-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="d281c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d281c-102">SYNOPSIS</span></span>
<span data-ttu-id="d281c-103">Восстановление удаленного секрета из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="d281c-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="d281c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d281c-104">SYNTAX</span></span>

### <span data-ttu-id="d281c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d281c-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d281c-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d281c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d281c-107">DESCRIPTION</span></span>
<span data-ttu-id="d281c-108">Командлет **Undo-AzKeyVaultSecretRemoval** восстановит ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="d281c-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="d281c-109">Восстановленный секрет будет активен и может использоваться для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="d281c-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="d281c-110">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="d281c-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d281c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d281c-111">EXAMPLES</span></span>

### <span data-ttu-id="d281c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d281c-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="d281c-113">Эта команда восстановит секретный "MySecret", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="d281c-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d281c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d281c-114">PARAMETERS</span></span>

### <span data-ttu-id="d281c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d281c-115">-DefaultProfile</span></span>
<span data-ttu-id="d281c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d281c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d281c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d281c-117">-InputObject</span></span>
<span data-ttu-id="d281c-118">Удален секретный объект</span><span class="sxs-lookup"><span data-stu-id="d281c-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d281c-119">-Name</span></span>
<span data-ttu-id="d281c-120">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="d281c-120">Secret name.</span></span>
<span data-ttu-id="d281c-121">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="d281c-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d281c-122">-VaultName</span></span>
<span data-ttu-id="d281c-123">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="d281c-123">Vault name.</span></span>
<span data-ttu-id="d281c-124">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="d281c-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d281c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d281c-125">-Confirm</span></span>
<span data-ttu-id="d281c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d281c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d281c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d281c-127">-WhatIf</span></span>
<span data-ttu-id="d281c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d281c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d281c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d281c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d281c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d281c-130">CommonParameters</span></span>
<span data-ttu-id="d281c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d281c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d281c-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d281c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d281c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d281c-133">INPUTS</span></span>

### <span data-ttu-id="d281c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d281c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="d281c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d281c-135">OUTPUTS</span></span>

### <span data-ttu-id="d281c-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d281c-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="d281c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d281c-137">NOTES</span></span>

## <span data-ttu-id="d281c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d281c-138">RELATED LINKS</span></span>

[<span data-ttu-id="d281c-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d281c-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="d281c-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d281c-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="d281c-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d281c-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
