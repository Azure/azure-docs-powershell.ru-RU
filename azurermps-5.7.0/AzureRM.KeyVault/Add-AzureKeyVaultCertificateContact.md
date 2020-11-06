---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568577"
---
# <span data-ttu-id="39556-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="39556-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="39556-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39556-102">SYNOPSIS</span></span>
<span data-ttu-id="39556-103">Добавляет контакт для уведомлений сертификата.</span><span class="sxs-lookup"><span data-stu-id="39556-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39556-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39556-104">SYNTAX</span></span>

### <span data-ttu-id="39556-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39556-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39556-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="39556-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39556-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39556-107">DESCRIPTION</span></span>
<span data-ttu-id="39556-108">Командлет **Add-AzureKeyVaultCertificateContact** добавляет контакт для хранилища ключей для уведомлений сертификата в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="39556-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="39556-109">Контакт получит обновления о таких событиях, как срок действия сертификата, например "закрыто", "сертификат обновлен" и т. д.</span><span class="sxs-lookup"><span data-stu-id="39556-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="39556-110">Эти события определяются политикой сертификата.</span><span class="sxs-lookup"><span data-stu-id="39556-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="39556-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39556-111">EXAMPLES</span></span>

### <span data-ttu-id="39556-112">Пример 1: Добавление контакта сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="39556-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="39556-113">Эта команда добавляет Patti Белова в качестве контакта сертификата для хранилища ключей ContosoKV01 и возвращает объект **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="39556-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="39556-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39556-114">PARAMETERS</span></span>

### <span data-ttu-id="39556-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39556-115">-DefaultProfile</span></span>
<span data-ttu-id="39556-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="39556-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39556-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="39556-117">-EmailAddress</span></span>
<span data-ttu-id="39556-118">Указывает адрес электронной почты контакта.</span><span class="sxs-lookup"><span data-stu-id="39556-118">Specifies the email address of the contact.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39556-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39556-119">-InputObject</span></span>
<span data-ttu-id="39556-120">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="39556-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39556-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39556-121">-PassThru</span></span>
<span data-ttu-id="39556-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="39556-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="39556-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="39556-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="39556-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="39556-124">-VaultName</span></span>
<span data-ttu-id="39556-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="39556-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39556-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39556-126">-Confirm</span></span>
<span data-ttu-id="39556-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39556-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39556-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39556-128">-WhatIf</span></span>
<span data-ttu-id="39556-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39556-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39556-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39556-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39556-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39556-131">CommonParameters</span></span>
<span data-ttu-id="39556-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39556-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39556-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39556-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39556-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39556-134">INPUTS</span></span>

### <span data-ttu-id="39556-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="39556-135">None</span></span>
<span data-ttu-id="39556-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="39556-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39556-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39556-137">OUTPUTS</span></span>

### <span data-ttu-id="39556-138">List<Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="39556-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="39556-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="39556-139">NOTES</span></span>

## <span data-ttu-id="39556-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39556-140">RELATED LINKS</span></span>

[<span data-ttu-id="39556-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="39556-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="39556-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="39556-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

