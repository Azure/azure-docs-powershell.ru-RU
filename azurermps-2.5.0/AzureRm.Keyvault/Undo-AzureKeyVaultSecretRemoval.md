---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
ms.openlocfilehash: a025dc40a666f643a3e7e232a22451e73f3e60bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913870"
---
# <span data-ttu-id="b3e41-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="b3e41-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="b3e41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3e41-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e41-103">Восстановление удаленного секрета из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b3e41-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3e41-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3e41-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e41-106">Командлет **Undo-AzureKeyVaultSecretRemoval** восстановит ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="b3e41-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="b3e41-107">Восстановленный секрет будет активен и может использоваться для всех обычных секретных операций.</span><span class="sxs-lookup"><span data-stu-id="b3e41-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="b3e41-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="b3e41-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b3e41-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3e41-109">EXAMPLES</span></span>

### <span data-ttu-id="b3e41-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3e41-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="b3e41-111">Эта команда восстановит секретный "MySecret", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="b3e41-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b3e41-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3e41-112">PARAMETERS</span></span>

### <span data-ttu-id="b3e41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e41-113">-DefaultProfile</span></span>
<span data-ttu-id="b3e41-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b3e41-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e41-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3e41-115">-Name</span></span>
<span data-ttu-id="b3e41-116">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="b3e41-116">Secret name.</span></span>
<span data-ttu-id="b3e41-117">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="b3e41-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="b3e41-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b3e41-118">-VaultName</span></span>
<span data-ttu-id="b3e41-119">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="b3e41-119">Vault name.</span></span>
<span data-ttu-id="b3e41-120">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="b3e41-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b3e41-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3e41-121">-Confirm</span></span>
<span data-ttu-id="b3e41-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3e41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e41-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e41-123">-WhatIf</span></span>
<span data-ttu-id="b3e41-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3e41-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e41-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3e41-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e41-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e41-126">CommonParameters</span></span>
<span data-ttu-id="b3e41-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3e41-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e41-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e41-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e41-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3e41-129">INPUTS</span></span>

### <span data-ttu-id="b3e41-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e41-130">System.String</span></span>

## <span data-ttu-id="b3e41-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3e41-131">OUTPUTS</span></span>

### <span data-ttu-id="b3e41-132">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="b3e41-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="b3e41-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3e41-133">NOTES</span></span>

## <span data-ttu-id="b3e41-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3e41-134">RELATED LINKS</span></span>

[<span data-ttu-id="b3e41-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b3e41-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)



[<span data-ttu-id="b3e41-136">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b3e41-136">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
