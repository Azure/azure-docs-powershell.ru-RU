---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9bfb62388ce4a7a8994f4a618a4c1a00ac5868d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913345"
---
# <span data-ttu-id="55896-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="55896-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="55896-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55896-102">SYNOPSIS</span></span>
<span data-ttu-id="55896-103">Удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="55896-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55896-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55896-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55896-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55896-105">DESCRIPTION</span></span>
<span data-ttu-id="55896-106">Командлет **Remove-AzureKeyVaultCertificateContact** удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="55896-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="55896-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55896-107">EXAMPLES</span></span>

### <span data-ttu-id="55896-108">Пример 1: Удаление контакта сертификата</span><span class="sxs-lookup"><span data-stu-id="55896-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="55896-109">Эта команда удаляет Patti Белова в качестве контакта сертификата для хранилища ключей Contoso01.</span><span class="sxs-lookup"><span data-stu-id="55896-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="55896-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55896-110">PARAMETERS</span></span>

### <span data-ttu-id="55896-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55896-111">-DefaultProfile</span></span>
<span data-ttu-id="55896-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55896-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55896-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="55896-113">-EmailAddress</span></span>
<span data-ttu-id="55896-114">Указывает адрес электронной почты контакта, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="55896-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55896-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55896-115">-PassThru</span></span>
<span data-ttu-id="55896-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="55896-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55896-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="55896-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55896-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="55896-118">-VaultName</span></span>
<span data-ttu-id="55896-119">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="55896-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="55896-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55896-120">-Confirm</span></span>
<span data-ttu-id="55896-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55896-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55896-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55896-122">-WhatIf</span></span>
<span data-ttu-id="55896-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55896-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55896-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55896-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55896-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55896-125">CommonParameters</span></span>
<span data-ttu-id="55896-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55896-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55896-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55896-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55896-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55896-128">INPUTS</span></span>

## <span data-ttu-id="55896-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55896-129">OUTPUTS</span></span>

### <span data-ttu-id="55896-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="55896-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="55896-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="55896-131">NOTES</span></span>

## <span data-ttu-id="55896-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55896-132">RELATED LINKS</span></span>

[<span data-ttu-id="55896-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="55896-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="55896-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="55896-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

