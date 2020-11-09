---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318536"
---
# <span data-ttu-id="568b3-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="568b3-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="568b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="568b3-102">SYNOPSIS</span></span>
<span data-ttu-id="568b3-103">Проверяет, доступен ли доменное имя в зоне cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="568b3-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="568b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="568b3-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="568b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="568b3-105">DESCRIPTION</span></span>
<span data-ttu-id="568b3-106">Проверяет, доступен ли доменное имя в зоне cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="568b3-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="568b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="568b3-107">EXAMPLES</span></span>

### <span data-ttu-id="568b3-108">Пример 1: Проверка доступности contoso.westus.cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="568b3-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="568b3-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="568b3-109">PARAMETERS</span></span>

### <span data-ttu-id="568b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568b3-110">-DefaultProfile</span></span>
<span data-ttu-id="568b3-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="568b3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="568b3-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="568b3-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="568b3-113">-Location</span><span class="sxs-lookup"><span data-stu-id="568b3-113">-Location</span></span>
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

### <span data-ttu-id="568b3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568b3-114">CommonParameters</span></span>
<span data-ttu-id="568b3-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="568b3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568b3-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="568b3-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568b3-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="568b3-117">INPUTS</span></span>

### <span data-ttu-id="568b3-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="568b3-118">None</span></span>

## <span data-ttu-id="568b3-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="568b3-119">OUTPUTS</span></span>

### <span data-ttu-id="568b3-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="568b3-120">System.Boolean</span></span>

## <span data-ttu-id="568b3-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="568b3-121">NOTES</span></span>

## <span data-ttu-id="568b3-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="568b3-122">RELATED LINKS</span></span>
