---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732370"
---
# <span data-ttu-id="885ce-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="885ce-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="885ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="885ce-102">SYNOPSIS</span></span>
<span data-ttu-id="885ce-103">Возвращает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="885ce-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="885ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="885ce-104">SYNTAX</span></span>

### <span data-ttu-id="885ce-105">VaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="885ce-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="885ce-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="885ce-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="885ce-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="885ce-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="885ce-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="885ce-108">DESCRIPTION</span></span>
<span data-ttu-id="885ce-109">Командлет **Get-AzureKeyVaultCertificateContact** получает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="885ce-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="885ce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="885ce-110">EXAMPLES</span></span>

### <span data-ttu-id="885ce-111">Пример 1: получение всех контактов сертификата</span><span class="sxs-lookup"><span data-stu-id="885ce-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="885ce-112">Эта команда получает все контакты для объектов сертификата в хранилище ключей Contoso, а затем сохраняет их в переменной $Contacts.</span><span class="sxs-lookup"><span data-stu-id="885ce-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="885ce-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="885ce-113">PARAMETERS</span></span>

### <span data-ttu-id="885ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885ce-114">-DefaultProfile</span></span>
<span data-ttu-id="885ce-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="885ce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="885ce-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="885ce-116">-InputObject</span></span>
<span data-ttu-id="885ce-117">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="885ce-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="885ce-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="885ce-118">-ResourceId</span></span>
<span data-ttu-id="885ce-119">Идентификатор KeyVault.</span><span class="sxs-lookup"><span data-stu-id="885ce-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="885ce-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="885ce-120">-VaultName</span></span>
<span data-ttu-id="885ce-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="885ce-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="885ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885ce-122">CommonParameters</span></span>
<span data-ttu-id="885ce-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="885ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885ce-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="885ce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885ce-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="885ce-125">INPUTS</span></span>

### <span data-ttu-id="885ce-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="885ce-126">None</span></span>
<span data-ttu-id="885ce-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="885ce-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="885ce-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="885ce-128">OUTPUTS</span></span>

### <span data-ttu-id="885ce-129">List<Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="885ce-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="885ce-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="885ce-130">NOTES</span></span>

## <span data-ttu-id="885ce-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="885ce-131">RELATED LINKS</span></span>

[<span data-ttu-id="885ce-132">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="885ce-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="885ce-133">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="885ce-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

