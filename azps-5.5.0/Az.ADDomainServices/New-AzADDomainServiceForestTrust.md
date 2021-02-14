---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: 91d7b92b7b52df20d69f53cddb98d6b9276b0b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210665"
---
# <span data-ttu-id="f624c-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="f624c-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="f624c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f624c-102">SYNOPSIS</span></span>
<span data-ttu-id="f624c-103">Создание объекта в памяти для ForestTrust</span><span class="sxs-lookup"><span data-stu-id="f624c-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="f624c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f624c-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="f624c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f624c-105">DESCRIPTION</span></span>
<span data-ttu-id="f624c-106">Создание объекта в памяти для ForestTrust</span><span class="sxs-lookup"><span data-stu-id="f624c-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="f624c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f624c-107">EXAMPLES</span></span>

### <span data-ttu-id="f624c-108">Пример 1. Создание ServiceForestTrust для ADDomain</span><span class="sxs-lookup"><span data-stu-id="f624c-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="f624c-109">Создание ServiceForestTrust для ADDomain</span><span class="sxs-lookup"><span data-stu-id="f624c-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="f624c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f624c-110">PARAMETERS</span></span>

### <span data-ttu-id="f624c-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f624c-111">-FriendlyName</span></span>
<span data-ttu-id="f624c-112">"Имя".</span><span class="sxs-lookup"><span data-stu-id="f624c-112">Friendly Name.</span></span>

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

### <span data-ttu-id="f624c-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="f624c-113">-RemoteDnsIP</span></span>
<span data-ttu-id="f624c-114">Ips удаленных DNS-адресов.</span><span class="sxs-lookup"><span data-stu-id="f624c-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="f624c-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="f624c-115">-TrustDirection</span></span>
<span data-ttu-id="f624c-116">Направление доверия.</span><span class="sxs-lookup"><span data-stu-id="f624c-116">Trust Direction.</span></span>

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

### <span data-ttu-id="f624c-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="f624c-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="f624c-118">FQDN надежного домена.</span><span class="sxs-lookup"><span data-stu-id="f624c-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="f624c-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="f624c-119">-TrustPassword</span></span>
<span data-ttu-id="f624c-120">Trust Password.</span><span class="sxs-lookup"><span data-stu-id="f624c-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f624c-121">CommonParameters</span></span>
<span data-ttu-id="f624c-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f624c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f624c-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f624c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f624c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f624c-124">INPUTS</span></span>

## <span data-ttu-id="f624c-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f624c-125">OUTPUTS</span></span>

### <span data-ttu-id="f624c-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="f624c-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="f624c-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f624c-127">NOTES</span></span>

<span data-ttu-id="f624c-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f624c-128">ALIASES</span></span>

## <span data-ttu-id="f624c-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f624c-129">RELATED LINKS</span></span>

