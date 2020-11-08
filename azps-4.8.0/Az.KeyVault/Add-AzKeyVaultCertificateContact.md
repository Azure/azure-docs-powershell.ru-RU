---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236211"
---
# <span data-ttu-id="9bdc9-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9bdc9-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="9bdc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bdc9-102">SYNOPSIS</span></span>
<span data-ttu-id="9bdc9-103">Добавляет контакт для уведомлений сертификата.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="9bdc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bdc9-104">SYNTAX</span></span>

### <span data-ttu-id="9bdc9-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bdc9-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bdc9-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="9bdc9-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bdc9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9bdc9-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bdc9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bdc9-108">DESCRIPTION</span></span>
<span data-ttu-id="9bdc9-109">Командлет **Add-AzKeyVaultCertificateContact** добавляет контакт для хранилища ключей для уведомлений сертификата в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="9bdc9-110">Контакт получит обновления о таких событиях, как срок действия сертификата, например "закрыто", "сертификат обновлен" и т. д.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="9bdc9-111">Эти события определяются политикой сертификата.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="9bdc9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bdc9-112">EXAMPLES</span></span>

### <span data-ttu-id="9bdc9-113">Пример 1: Добавление контакта сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="9bdc9-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="9bdc9-114">Эта команда добавляет Patti Белова в качестве контакта сертификата для хранилища ключей ContosoKV01 и возвращает список контактов для хранилища "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="9bdc9-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="9bdc9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bdc9-115">PARAMETERS</span></span>

### <span data-ttu-id="9bdc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bdc9-116">-DefaultProfile</span></span>
<span data-ttu-id="9bdc9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9bdc9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bdc9-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9bdc9-118">-EmailAddress</span></span>
<span data-ttu-id="9bdc9-119">Указывает адрес электронной почты контакта.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bdc9-120">-InputObject</span></span>
<span data-ttu-id="9bdc9-121">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bdc9-122">-PassThru</span></span>
<span data-ttu-id="9bdc9-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9bdc9-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bdc9-125">-ResourceId</span></span>
<span data-ttu-id="9bdc9-126">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc9-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9bdc9-127">-VaultName</span></span>
<span data-ttu-id="9bdc9-128">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdc9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bdc9-129">-Confirm</span></span>
<span data-ttu-id="9bdc9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bdc9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bdc9-131">-WhatIf</span></span>
<span data-ttu-id="9bdc9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bdc9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bdc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bdc9-134">CommonParameters</span></span>
<span data-ttu-id="9bdc9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bdc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bdc9-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bdc9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bdc9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bdc9-137">INPUTS</span></span>

### <span data-ttu-id="9bdc9-138">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9bdc9-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9bdc9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9bdc9-139">System.String</span></span>

## <span data-ttu-id="9bdc9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bdc9-140">OUTPUTS</span></span>

### <span data-ttu-id="9bdc9-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9bdc9-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="9bdc9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bdc9-142">NOTES</span></span>

## <span data-ttu-id="9bdc9-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bdc9-143">RELATED LINKS</span></span>

[<span data-ttu-id="9bdc9-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9bdc9-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="9bdc9-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9bdc9-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

