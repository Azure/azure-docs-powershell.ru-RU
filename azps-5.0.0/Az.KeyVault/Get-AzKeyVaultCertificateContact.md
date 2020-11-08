---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250226"
---
# <span data-ttu-id="7f596-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7f596-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7f596-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f596-102">SYNOPSIS</span></span>
<span data-ttu-id="7f596-103">Возвращает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="7f596-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="7f596-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f596-104">SYNTAX</span></span>

### <span data-ttu-id="7f596-105">VaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f596-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f596-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7f596-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f596-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f596-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f596-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f596-108">DESCRIPTION</span></span>
<span data-ttu-id="7f596-109">Командлет **Get-AzKeyVaultCertificateContact** получает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7f596-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7f596-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f596-110">EXAMPLES</span></span>

### <span data-ttu-id="7f596-111">Пример 1: получение всех контактов сертификата</span><span class="sxs-lookup"><span data-stu-id="7f596-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="7f596-112">Эта команда получает все контакты для объектов сертификата в хранилище ключей Contoso, а затем сохраняет их в переменной $Contacts.</span><span class="sxs-lookup"><span data-stu-id="7f596-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="7f596-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f596-113">PARAMETERS</span></span>

### <span data-ttu-id="7f596-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f596-114">-DefaultProfile</span></span>
<span data-ttu-id="7f596-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7f596-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f596-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f596-116">-InputObject</span></span>
<span data-ttu-id="7f596-117">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7f596-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f596-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f596-118">-ResourceId</span></span>
<span data-ttu-id="7f596-119">Идентификатор KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7f596-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="7f596-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7f596-120">-VaultName</span></span>
<span data-ttu-id="7f596-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="7f596-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f596-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f596-122">CommonParameters</span></span>
<span data-ttu-id="7f596-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f596-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f596-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f596-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f596-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f596-125">INPUTS</span></span>

### <span data-ttu-id="7f596-126">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7f596-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="7f596-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7f596-127">System.String</span></span>

## <span data-ttu-id="7f596-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f596-128">OUTPUTS</span></span>

### <span data-ttu-id="7f596-129">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7f596-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7f596-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f596-130">NOTES</span></span>

## <span data-ttu-id="7f596-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f596-131">RELATED LINKS</span></span>

[<span data-ttu-id="7f596-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7f596-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="7f596-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7f596-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

