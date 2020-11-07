---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 6d6626164000957ffaa987a71131987f35a977c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729936"
---
# <span data-ttu-id="23929-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="23929-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="23929-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23929-102">SYNOPSIS</span></span>
<span data-ttu-id="23929-103">Проверяет, доступен ли доменное имя в зоне cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="23929-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="23929-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23929-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23929-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23929-105">DESCRIPTION</span></span>
<span data-ttu-id="23929-106">Проверяет, доступен ли доменное имя в зоне cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="23929-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="23929-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23929-107">EXAMPLES</span></span>

### <span data-ttu-id="23929-108">Пример 1: Проверка доступности contoso.cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="23929-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="23929-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23929-109">PARAMETERS</span></span>

### <span data-ttu-id="23929-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23929-110">-DefaultProfile</span></span>
<span data-ttu-id="23929-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23929-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23929-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="23929-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="23929-113">-Location</span><span class="sxs-lookup"><span data-stu-id="23929-113">-Location</span></span>
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

### <span data-ttu-id="23929-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23929-114">CommonParameters</span></span>
<span data-ttu-id="23929-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23929-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23929-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23929-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23929-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23929-117">INPUTS</span></span>

### <span data-ttu-id="23929-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="23929-118">None</span></span>

## <span data-ttu-id="23929-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23929-119">OUTPUTS</span></span>

### <span data-ttu-id="23929-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23929-120">System.Boolean</span></span>

## <span data-ttu-id="23929-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="23929-121">NOTES</span></span>

## <span data-ttu-id="23929-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23929-122">RELATED LINKS</span></span>
