---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 9c7b82c8ec884cc16bc3c593d9f00f1789b98e52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720674"
---
# <span data-ttu-id="bb879-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bb879-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="bb879-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb879-102">SYNOPSIS</span></span>
<span data-ttu-id="bb879-103">Возвращает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="bb879-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="bb879-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb879-104">SYNTAX</span></span>

### <span data-ttu-id="bb879-105">VaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb879-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb879-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb879-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb879-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb879-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb879-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb879-108">DESCRIPTION</span></span>
<span data-ttu-id="bb879-109">Командлет **Get-AzKeyVaultCertificateContact** получает контакты, которые зарегистрированы для уведомлений сертификата для хранилища ключей в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bb879-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="bb879-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb879-110">EXAMPLES</span></span>

### <span data-ttu-id="bb879-111">Пример 1: получение всех контактов сертификата</span><span class="sxs-lookup"><span data-stu-id="bb879-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="bb879-112">Эта команда получает все контакты для объектов сертификата в хранилище ключей Contoso, а затем сохраняет их в переменной $Contacts.</span><span class="sxs-lookup"><span data-stu-id="bb879-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="bb879-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb879-113">PARAMETERS</span></span>

### <span data-ttu-id="bb879-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb879-114">-DefaultProfile</span></span>
<span data-ttu-id="bb879-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb879-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb879-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb879-116">-InputObject</span></span>
<span data-ttu-id="bb879-117">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="bb879-117">KeyVault object.</span></span>

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

### <span data-ttu-id="bb879-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb879-118">-ResourceId</span></span>
<span data-ttu-id="bb879-119">Идентификатор KeyVault.</span><span class="sxs-lookup"><span data-stu-id="bb879-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="bb879-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bb879-120">-VaultName</span></span>
<span data-ttu-id="bb879-121">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="bb879-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="bb879-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb879-122">CommonParameters</span></span>
<span data-ttu-id="bb879-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb879-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb879-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb879-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb879-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb879-125">INPUTS</span></span>

### <span data-ttu-id="bb879-126">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bb879-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="bb879-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bb879-127">System.String</span></span>

## <span data-ttu-id="bb879-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb879-128">OUTPUTS</span></span>

### <span data-ttu-id="bb879-129">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bb879-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="bb879-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb879-130">NOTES</span></span>

## <span data-ttu-id="bb879-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb879-131">RELATED LINKS</span></span>

[<span data-ttu-id="bb879-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bb879-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="bb879-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bb879-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

