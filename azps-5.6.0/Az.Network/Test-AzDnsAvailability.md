---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: dbc21a337263bb0e509188d472e4ff984e22322b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951747"
---
# <span data-ttu-id="bbaad-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="bbaad-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="bbaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbaad-102">SYNOPSIS</span></span>
<span data-ttu-id="bbaad-103">Проверяет, доступно ли доменное имя в cloudapp.azure.com зоне.</span><span class="sxs-lookup"><span data-stu-id="bbaad-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="bbaad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbaad-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbaad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbaad-105">DESCRIPTION</span></span>
<span data-ttu-id="bbaad-106">Проверяет, доступно ли доменное имя в cloudapp.azure.com зоне.</span><span class="sxs-lookup"><span data-stu-id="bbaad-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="bbaad-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbaad-107">EXAMPLES</span></span>

### <span data-ttu-id="bbaad-108">Пример 1. Проверьте, contoso.westus.cloudapp.azure.com ли contoso.westus.cloudapp.azure.com можно использовать.</span><span class="sxs-lookup"><span data-stu-id="bbaad-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="bbaad-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbaad-109">PARAMETERS</span></span>

### <span data-ttu-id="bbaad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbaad-110">-DefaultProfile</span></span>
<span data-ttu-id="bbaad-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbaad-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbaad-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="bbaad-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbaad-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bbaad-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbaad-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbaad-114">CommonParameters</span></span>
<span data-ttu-id="bbaad-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbaad-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbaad-116">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbaad-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbaad-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbaad-117">INPUTS</span></span>

### <span data-ttu-id="bbaad-118">Нет</span><span class="sxs-lookup"><span data-stu-id="bbaad-118">None</span></span>

## <span data-ttu-id="bbaad-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbaad-119">OUTPUTS</span></span>

### <span data-ttu-id="bbaad-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbaad-120">System.Boolean</span></span>

## <span data-ttu-id="bbaad-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbaad-121">NOTES</span></span>

## <span data-ttu-id="bbaad-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbaad-122">RELATED LINKS</span></span>
