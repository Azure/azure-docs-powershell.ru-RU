---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734060"
---
# <span data-ttu-id="1f26e-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1f26e-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="1f26e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f26e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f26e-103">Возвращает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1f26e-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f26e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f26e-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f26e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f26e-105">DESCRIPTION</span></span>
<span data-ttu-id="1f26e-106">Командлет **Get-AzureKeyVaultCertificateContact** получает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f26e-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="1f26e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f26e-107">EXAMPLES</span></span>

### <span data-ttu-id="1f26e-108">Пример 1: получение всех контактов сертификата</span><span class="sxs-lookup"><span data-stu-id="1f26e-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="1f26e-109">Эта команда получает все контакты для объектов сертификата в хранилище ключей Contoso, а затем сохраняет их в переменной $Contacts.</span><span class="sxs-lookup"><span data-stu-id="1f26e-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="1f26e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f26e-110">PARAMETERS</span></span>

### <span data-ttu-id="1f26e-111">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1f26e-111">-VaultName</span></span>
<span data-ttu-id="1f26e-112">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1f26e-112">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f26e-113">-DefaultProfile</span></span>
<span data-ttu-id="1f26e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f26e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f26e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f26e-115">CommonParameters</span></span>
<span data-ttu-id="1f26e-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f26e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f26e-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f26e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f26e-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f26e-118">INPUTS</span></span>

## <span data-ttu-id="1f26e-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f26e-119">OUTPUTS</span></span>

### <span data-ttu-id="1f26e-120">List<Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="1f26e-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="1f26e-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f26e-121">NOTES</span></span>

## <span data-ttu-id="1f26e-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f26e-122">RELATED LINKS</span></span>

[<span data-ttu-id="1f26e-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1f26e-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="1f26e-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1f26e-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

