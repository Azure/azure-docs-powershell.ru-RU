---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323515"
---
# <span data-ttu-id="36e2c-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="36e2c-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="36e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="36e2c-103">Получает контакты, зарегистрированные для уведомлений о сертификате для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="36e2c-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="36e2c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36e2c-104">SYNTAX</span></span>

### <span data-ttu-id="36e2c-105">VaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36e2c-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36e2c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36e2c-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36e2c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36e2c-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36e2c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36e2c-108">DESCRIPTION</span></span>
<span data-ttu-id="36e2c-109">**Cmdlet Get-AzKeyVaultCertificateContact** возвращает контакты, зарегистрированные для уведомлений о сертификате для хранилища ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="36e2c-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="36e2c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="36e2c-111">Пример 1. Получить все контакты сертификата</span><span class="sxs-lookup"><span data-stu-id="36e2c-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="36e2c-112">Эта команда получает все контакты для объектов сертификата в хранилище ключей Contoso, а затем сохраняет их в $Contacts переменной.</span><span class="sxs-lookup"><span data-stu-id="36e2c-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="36e2c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36e2c-113">PARAMETERS</span></span>

### <span data-ttu-id="36e2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e2c-114">-DefaultProfile</span></span>
<span data-ttu-id="36e2c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36e2c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36e2c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e2c-116">-InputObject</span></span>
<span data-ttu-id="36e2c-117">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="36e2c-117">KeyVault object.</span></span>

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

### <span data-ttu-id="36e2c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36e2c-118">-ResourceId</span></span>
<span data-ttu-id="36e2c-119">KeyVault Id.</span><span class="sxs-lookup"><span data-stu-id="36e2c-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="36e2c-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="36e2c-120">-VaultName</span></span>
<span data-ttu-id="36e2c-121">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="36e2c-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="36e2c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e2c-122">CommonParameters</span></span>
<span data-ttu-id="36e2c-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e2c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e2c-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e2c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e2c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36e2c-125">INPUTS</span></span>

### <span data-ttu-id="36e2c-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="36e2c-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="36e2c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="36e2c-127">System.String</span></span>

## <span data-ttu-id="36e2c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36e2c-128">OUTPUTS</span></span>

### <span data-ttu-id="36e2c-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="36e2c-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="36e2c-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36e2c-130">NOTES</span></span>

## <span data-ttu-id="36e2c-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36e2c-131">RELATED LINKS</span></span>

[<span data-ttu-id="36e2c-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="36e2c-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="36e2c-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="36e2c-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

