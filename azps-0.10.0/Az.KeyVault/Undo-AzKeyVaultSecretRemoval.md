---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399096"
---
# <span data-ttu-id="22d05-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="22d05-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="22d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d05-102">SYNOPSIS</span></span>
<span data-ttu-id="22d05-103">Восстановление удаленной секретной секретной области в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="22d05-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="22d05-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22d05-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d05-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22d05-105">DESCRIPTION</span></span>
<span data-ttu-id="22d05-106">С **его нажатием** можно восстановить ранее удаленную секретную.</span><span class="sxs-lookup"><span data-stu-id="22d05-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="22d05-107">Восстановленная секретная будет активна и ее можно использовать для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="22d05-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="22d05-108">Для выполнения этой операции вызываемму вызываемму звоня необходимо разрешение на восстановление.</span><span class="sxs-lookup"><span data-stu-id="22d05-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="22d05-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22d05-109">EXAMPLES</span></span>

### <span data-ttu-id="22d05-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22d05-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="22d05-111">Эта команда восстановит секретный "МойСекрет", который ранее был удален, в активное и можное состояние.</span><span class="sxs-lookup"><span data-stu-id="22d05-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="22d05-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22d05-112">PARAMETERS</span></span>

### <span data-ttu-id="22d05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d05-113">-DefaultProfile</span></span>
<span data-ttu-id="22d05-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="22d05-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d05-115">-Name</span><span class="sxs-lookup"><span data-stu-id="22d05-115">-Name</span></span>
<span data-ttu-id="22d05-116">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="22d05-116">Secret name.</span></span>
<span data-ttu-id="22d05-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="22d05-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d05-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="22d05-118">-VaultName</span></span>
<span data-ttu-id="22d05-119">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="22d05-119">Vault name.</span></span>
<span data-ttu-id="22d05-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="22d05-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d05-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22d05-121">-Confirm</span></span>
<span data-ttu-id="22d05-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="22d05-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d05-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d05-123">-WhatIf</span></span>
<span data-ttu-id="22d05-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22d05-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d05-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22d05-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d05-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d05-126">CommonParameters</span></span>
<span data-ttu-id="22d05-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d05-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d05-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d05-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d05-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22d05-129">INPUTS</span></span>

### <span data-ttu-id="22d05-130">System.String</span><span class="sxs-lookup"><span data-stu-id="22d05-130">System.String</span></span>

## <span data-ttu-id="22d05-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22d05-131">OUTPUTS</span></span>

### <span data-ttu-id="22d05-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span><span class="sxs-lookup"><span data-stu-id="22d05-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="22d05-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22d05-133">NOTES</span></span>

## <span data-ttu-id="22d05-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22d05-134">RELATED LINKS</span></span>

[<span data-ttu-id="22d05-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="22d05-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="22d05-136">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="22d05-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
