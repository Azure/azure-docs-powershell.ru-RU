---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565838"
---
# <span data-ttu-id="b0df9-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="b0df9-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="b0df9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0df9-102">SYNOPSIS</span></span>
<span data-ttu-id="b0df9-103">Проверяет, доступен ли доменное имя в зоне cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="b0df9-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0df9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0df9-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0df9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0df9-105">DESCRIPTION</span></span>
<span data-ttu-id="b0df9-106">Проверяет, доступен ли доменное имя в зоне cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="b0df9-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="b0df9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0df9-107">EXAMPLES</span></span>

### <span data-ttu-id="b0df9-108">Пример 1: Проверка доступности contoso.cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="b0df9-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="b0df9-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0df9-109">PARAMETERS</span></span>

### <span data-ttu-id="b0df9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0df9-110">-DefaultProfile</span></span>
<span data-ttu-id="b0df9-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0df9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0df9-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b0df9-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="b0df9-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b0df9-113">-Location</span></span>
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

### <span data-ttu-id="b0df9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0df9-114">CommonParameters</span></span>
<span data-ttu-id="b0df9-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0df9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0df9-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0df9-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0df9-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0df9-117">INPUTS</span></span>

### <span data-ttu-id="b0df9-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="b0df9-118">None</span></span>

## <span data-ttu-id="b0df9-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0df9-119">OUTPUTS</span></span>

### <span data-ttu-id="b0df9-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0df9-120">System.Boolean</span></span>

## <span data-ttu-id="b0df9-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0df9-121">NOTES</span></span>

## <span data-ttu-id="b0df9-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0df9-122">RELATED LINKS</span></span>
