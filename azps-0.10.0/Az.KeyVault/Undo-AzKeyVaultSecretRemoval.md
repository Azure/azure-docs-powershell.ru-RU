---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911144"
---
# <span data-ttu-id="3e4e3-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="3e4e3-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="3e4e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e4e3-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4e3-103">Восстановление удаленного секрета из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="3e4e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e4e3-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e4e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4e3-105">DESCRIPTION</span></span>
<span data-ttu-id="3e4e3-106">Командлет **Undo-AzKeyVaultSecretRemoval** восстановит ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="3e4e3-107">Восстановленный секрет будет активен и может использоваться для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="3e4e3-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="3e4e3-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="3e4e3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e4e3-109">EXAMPLES</span></span>

### <span data-ttu-id="3e4e3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e4e3-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="3e4e3-111">Эта команда восстановит секретный "MySecret", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="3e4e3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e4e3-112">PARAMETERS</span></span>

### <span data-ttu-id="3e4e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4e3-113">-DefaultProfile</span></span>
<span data-ttu-id="3e4e3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e4e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e4e3-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e4e3-115">-Name</span></span>
<span data-ttu-id="3e4e3-116">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-116">Secret name.</span></span>
<span data-ttu-id="3e4e3-117">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="3e4e3-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3e4e3-118">-VaultName</span></span>
<span data-ttu-id="3e4e3-119">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-119">Vault name.</span></span>
<span data-ttu-id="3e4e3-120">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3e4e3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e4e3-121">-Confirm</span></span>
<span data-ttu-id="3e4e3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e4e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e4e3-123">-WhatIf</span></span>
<span data-ttu-id="3e4e3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e4e3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e4e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4e3-126">CommonParameters</span></span>
<span data-ttu-id="3e4e3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e4e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4e3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e4e3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4e3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e4e3-129">INPUTS</span></span>

### <span data-ttu-id="3e4e3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e4e3-130">System.String</span></span>

## <span data-ttu-id="3e4e3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4e3-131">OUTPUTS</span></span>

### <span data-ttu-id="3e4e3-132">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="3e4e3-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="3e4e3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e4e3-133">NOTES</span></span>

## <span data-ttu-id="3e4e3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e4e3-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e4e3-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3e4e3-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="3e4e3-136">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3e4e3-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="3e4e3-137">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3e4e3-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
