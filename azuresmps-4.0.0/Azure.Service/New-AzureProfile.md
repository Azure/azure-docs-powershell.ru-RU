---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076000"
---
# <span data-ttu-id="e62aa-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="e62aa-101">New-AzureProfile</span></span>

## <span data-ttu-id="e62aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e62aa-102">SYNOPSIS</span></span>

## <span data-ttu-id="e62aa-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e62aa-103">SYNTAX</span></span>

### <span data-ttu-id="e62aa-104">См</span><span class="sxs-lookup"><span data-stu-id="e62aa-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="e62aa-105">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e62aa-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="e62aa-106">Аппарат</span><span class="sxs-lookup"><span data-stu-id="e62aa-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="e62aa-107">Записи</span><span class="sxs-lookup"><span data-stu-id="e62aa-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="e62aa-108">Очистку</span><span class="sxs-lookup"><span data-stu-id="e62aa-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="e62aa-109">Файл</span><span class="sxs-lookup"><span data-stu-id="e62aa-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="e62aa-110">Контейнер</span><span class="sxs-lookup"><span data-stu-id="e62aa-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="e62aa-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e62aa-111">DESCRIPTION</span></span>

## <span data-ttu-id="e62aa-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e62aa-112">EXAMPLES</span></span>

### <span data-ttu-id="e62aa-113">1:</span><span class="sxs-lookup"><span data-stu-id="e62aa-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e62aa-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e62aa-114">PARAMETERS</span></span>

### <span data-ttu-id="e62aa-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="e62aa-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="e62aa-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="e62aa-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="e62aa-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-119">-Environment</span><span class="sxs-lookup"><span data-stu-id="e62aa-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-120">-Path</span><span class="sxs-lookup"><span data-stu-id="e62aa-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-121">-Свойства</span><span class="sxs-lookup"><span data-stu-id="e62aa-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-122">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e62aa-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e62aa-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e62aa-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-125">-Клиент</span><span class="sxs-lookup"><span data-stu-id="e62aa-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62aa-126">CommonParameters</span></span>
<span data-ttu-id="e62aa-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e62aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62aa-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e62aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62aa-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e62aa-129">INPUTS</span></span>

## <span data-ttu-id="e62aa-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e62aa-130">OUTPUTS</span></span>

## <span data-ttu-id="e62aa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e62aa-131">NOTES</span></span>

## <span data-ttu-id="e62aa-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e62aa-132">RELATED LINKS</span></span>

