---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235971"
---
# <span data-ttu-id="29891-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="29891-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="29891-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29891-102">SYNOPSIS</span></span>
<span data-ttu-id="29891-103">**Тест-AzPrivateLinkServiceVisibility** проверяет, является ли служба частной ссылки видимой для текущего использования.</span><span class="sxs-lookup"><span data-stu-id="29891-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="29891-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29891-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29891-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29891-105">DESCRIPTION</span></span>
<span data-ttu-id="29891-106">Проверьте, является ли служба частной ссылки видимой для текущего использования.</span><span class="sxs-lookup"><span data-stu-id="29891-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="29891-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29891-107">EXAMPLES</span></span>

### <span data-ttu-id="29891-108">Пример 1: Проверка доступности contoso.cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="29891-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="29891-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29891-109">PARAMETERS</span></span>

### <span data-ttu-id="29891-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29891-110">-DefaultProfile</span></span>
<span data-ttu-id="29891-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29891-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29891-112">-Location</span><span class="sxs-lookup"><span data-stu-id="29891-112">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29891-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="29891-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="29891-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29891-114">-ResourceGroupName</span></span>
<span data-ttu-id="29891-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29891-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29891-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29891-116">CommonParameters</span></span>
<span data-ttu-id="29891-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29891-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29891-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29891-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29891-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29891-119">INPUTS</span></span>

### <span data-ttu-id="29891-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="29891-120">None</span></span>

## <span data-ttu-id="29891-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29891-121">OUTPUTS</span></span>

### <span data-ttu-id="29891-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29891-122">System.Boolean</span></span>

## <span data-ttu-id="29891-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="29891-123">NOTES</span></span>

## <span data-ttu-id="29891-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29891-124">RELATED LINKS</span></span>
