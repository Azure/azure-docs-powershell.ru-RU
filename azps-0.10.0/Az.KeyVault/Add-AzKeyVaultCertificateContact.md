---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911184"
---
# <span data-ttu-id="3e1d4-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3e1d4-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3e1d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1d4-103">Добавляет контакт для уведомлений сертификата.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="3e1d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e1d4-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e1d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e1d4-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1d4-106">Командлет **Add-AzKeyVaultCertificateContact** добавляет контакт для хранилища ключей для уведомлений сертификата в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="3e1d4-107">Контакт получит обновления о таких событиях, как срок действия сертификата, например "закрыто", "сертификат обновлен" и т. д.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="3e1d4-108">Эти события определяются политикой сертификата.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="3e1d4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e1d4-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1d4-110">Пример 1: Добавление контакта сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="3e1d4-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="3e1d4-111">Эта команда добавляет Patti Белова в качестве контакта сертификата для хранилища ключей ContosoKV01 и возвращает объект **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="3e1d4-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="3e1d4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e1d4-112">PARAMETERS</span></span>

### <span data-ttu-id="3e1d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1d4-113">-DefaultProfile</span></span>
<span data-ttu-id="3e1d4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e1d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e1d4-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3e1d4-115">-EmailAddress</span></span>
<span data-ttu-id="3e1d4-116">Указывает адрес электронной почты контакта.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="3e1d4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e1d4-117">-PassThru</span></span>
<span data-ttu-id="3e1d4-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e1d4-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e1d4-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3e1d4-120">-VaultName</span></span>
<span data-ttu-id="3e1d4-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="3e1d4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e1d4-122">-Confirm</span></span>
<span data-ttu-id="3e1d4-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1d4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1d4-124">-WhatIf</span></span>
<span data-ttu-id="3e1d4-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1d4-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1d4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1d4-127">CommonParameters</span></span>
<span data-ttu-id="3e1d4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1d4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1d4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1d4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e1d4-130">INPUTS</span></span>

### <span data-ttu-id="3e1d4-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="3e1d4-131">None</span></span>
<span data-ttu-id="3e1d4-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3e1d4-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e1d4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e1d4-133">OUTPUTS</span></span>

### <span data-ttu-id="3e1d4-134">List<Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="3e1d4-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="3e1d4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e1d4-135">NOTES</span></span>

## <span data-ttu-id="3e1d4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e1d4-136">RELATED LINKS</span></span>

[<span data-ttu-id="3e1d4-137">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3e1d4-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="3e1d4-138">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3e1d4-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

