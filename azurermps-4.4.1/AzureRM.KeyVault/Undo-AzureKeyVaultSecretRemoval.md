---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733722"
---
# <span data-ttu-id="4aa34-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="4aa34-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="4aa34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4aa34-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa34-103">Восстановление удаленного секрета из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4aa34-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aa34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4aa34-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aa34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aa34-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa34-106">Командлет **Undo-AzureKeyVaultSecretRemoval** восстановит ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="4aa34-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="4aa34-107">Восстановленный секрет будет активен и может использоваться для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="4aa34-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="4aa34-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="4aa34-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="4aa34-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4aa34-109">EXAMPLES</span></span>

### <span data-ttu-id="4aa34-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4aa34-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="4aa34-111">Эта команда восстановит секретный "MySecret", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="4aa34-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="4aa34-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4aa34-112">PARAMETERS</span></span>

### <span data-ttu-id="4aa34-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4aa34-113">-Name</span></span>
<span data-ttu-id="4aa34-114">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="4aa34-114">Secret name.</span></span>
<span data-ttu-id="4aa34-115">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="4aa34-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa34-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4aa34-116">-VaultName</span></span>
<span data-ttu-id="4aa34-117">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="4aa34-117">Vault name.</span></span>
<span data-ttu-id="4aa34-118">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="4aa34-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa34-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aa34-119">-Confirm</span></span>
<span data-ttu-id="4aa34-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4aa34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa34-121">-WhatIf</span></span>
<span data-ttu-id="4aa34-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4aa34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa34-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4aa34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa34-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa34-124">-DefaultProfile</span></span>
<span data-ttu-id="4aa34-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa34-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aa34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa34-126">CommonParameters</span></span>
<span data-ttu-id="4aa34-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4aa34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa34-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa34-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa34-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4aa34-129">INPUTS</span></span>

### <span data-ttu-id="4aa34-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4aa34-130">System.String</span></span>

## <span data-ttu-id="4aa34-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aa34-131">OUTPUTS</span></span>

### <span data-ttu-id="4aa34-132">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="4aa34-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="4aa34-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4aa34-133">NOTES</span></span>

## <span data-ttu-id="4aa34-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4aa34-134">RELATED LINKS</span></span>

[<span data-ttu-id="4aa34-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4aa34-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="4aa34-136">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4aa34-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="4aa34-137">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4aa34-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
