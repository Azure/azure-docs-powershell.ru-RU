---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: d6d2070afcb4a5b9b0b13af1fa54dc93621c5a97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913874"
---
# <span data-ttu-id="6e448-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6e448-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="6e448-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e448-102">SYNOPSIS</span></span>
<span data-ttu-id="6e448-103">Возвращает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="6e448-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e448-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e448-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e448-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e448-105">DESCRIPTION</span></span>
<span data-ttu-id="6e448-106">Командлет **Get-AzureKeyVaultCertificateContact** получает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="6e448-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6e448-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e448-107">EXAMPLES</span></span>

### <span data-ttu-id="6e448-108">Пример 1: получение всех контактов сертификата</span><span class="sxs-lookup"><span data-stu-id="6e448-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="6e448-109">Эта команда получает все контакты для объектов сертификата в хранилище ключей Contoso, а затем сохраняет их в переменной $Contacts.</span><span class="sxs-lookup"><span data-stu-id="6e448-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="6e448-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e448-110">PARAMETERS</span></span>

### <span data-ttu-id="6e448-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e448-111">-DefaultProfile</span></span>
<span data-ttu-id="6e448-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6e448-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e448-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6e448-113">-VaultName</span></span>
<span data-ttu-id="6e448-114">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="6e448-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="6e448-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e448-115">CommonParameters</span></span>
<span data-ttu-id="6e448-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e448-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e448-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e448-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e448-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e448-118">INPUTS</span></span>

## <span data-ttu-id="6e448-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e448-119">OUTPUTS</span></span>

### <span data-ttu-id="6e448-120">List<Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="6e448-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="6e448-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e448-121">NOTES</span></span>

## <span data-ttu-id="6e448-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e448-122">RELATED LINKS</span></span>

[<span data-ttu-id="6e448-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6e448-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="6e448-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="6e448-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

