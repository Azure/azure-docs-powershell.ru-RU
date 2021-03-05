---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994493"
---
# <span data-ttu-id="32ad0-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="32ad0-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="32ad0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="32ad0-103">Создание объекта в памяти для группы "Секретная группа сейфа"</span><span class="sxs-lookup"><span data-stu-id="32ad0-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="32ad0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32ad0-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="32ad0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="32ad0-106">Создание объекта в памяти для секретной группы</span><span class="sxs-lookup"><span data-stu-id="32ad0-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="32ad0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32ad0-107">EXAMPLES</span></span>

### <span data-ttu-id="32ad0-108">Пример 1. Создание сейфа секретного объекта группы</span><span class="sxs-lookup"><span data-stu-id="32ad0-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="32ad0-109">Эта команда создает секретный объект группы сейфа, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="32ad0-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="32ad0-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="32ad0-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="32ad0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32ad0-111">PARAMETERS</span></span>

### <span data-ttu-id="32ad0-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="32ad0-112">-CertificateUrl</span></span>
<span data-ttu-id="32ad0-113">Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.</span><span class="sxs-lookup"><span data-stu-id="32ad0-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ad0-114">-Id</span><span class="sxs-lookup"><span data-stu-id="32ad0-114">-Id</span></span>
<span data-ttu-id="32ad0-115">ИД ресурса хранилища ключевых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="32ad0-115">Key Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ad0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ad0-116">CommonParameters</span></span>
<span data-ttu-id="32ad0-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32ad0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ad0-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32ad0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ad0-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32ad0-119">INPUTS</span></span>

## <span data-ttu-id="32ad0-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32ad0-120">OUTPUTS</span></span>

### <span data-ttu-id="32ad0-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="32ad0-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="32ad0-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32ad0-122">NOTES</span></span>

<span data-ttu-id="32ad0-123">ALIASES</span><span class="sxs-lookup"><span data-stu-id="32ad0-123">ALIASES</span></span>

## <span data-ttu-id="32ad0-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32ad0-124">RELATED LINKS</span></span>

