---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910309"
---
# <span data-ttu-id="3ecd9-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3ecd9-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3ecd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ecd9-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecd9-103">Возвращает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3ecd9-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="3ecd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ecd9-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ecd9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ecd9-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecd9-106">Командлет **Get-AzKeyVaultCertificateContact** получает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3ecd9-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="3ecd9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ecd9-107">EXAMPLES</span></span>

### <span data-ttu-id="3ecd9-108">Пример 1: получение всех контактов сертификата</span><span class="sxs-lookup"><span data-stu-id="3ecd9-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="3ecd9-109">Эта команда получает все контакты для объектов сертификата в хранилище ключей Contoso, а затем сохраняет их в переменной $Contacts.</span><span class="sxs-lookup"><span data-stu-id="3ecd9-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="3ecd9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ecd9-110">PARAMETERS</span></span>

### <span data-ttu-id="3ecd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecd9-111">-DefaultProfile</span></span>
<span data-ttu-id="3ecd9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ecd9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ecd9-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3ecd9-113">-VaultName</span></span>
<span data-ttu-id="3ecd9-114">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3ecd9-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="3ecd9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecd9-115">CommonParameters</span></span>
<span data-ttu-id="3ecd9-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ecd9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecd9-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecd9-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecd9-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ecd9-118">INPUTS</span></span>

### <span data-ttu-id="3ecd9-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ecd9-119">None</span></span>
<span data-ttu-id="3ecd9-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3ecd9-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ecd9-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ecd9-121">OUTPUTS</span></span>

### <span data-ttu-id="3ecd9-122">List<Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="3ecd9-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="3ecd9-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ecd9-123">NOTES</span></span>

## <span data-ttu-id="3ecd9-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ecd9-124">RELATED LINKS</span></span>

[<span data-ttu-id="3ecd9-125">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3ecd9-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="3ecd9-126">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3ecd9-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

