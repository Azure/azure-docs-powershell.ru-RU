---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: 3fe05034734a4cfb0d511921372e41b00d7b457c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951715"
---
# <span data-ttu-id="be331-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="be331-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="be331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be331-102">SYNOPSIS</span></span>
<span data-ttu-id="be331-103">**Тест-AzPrivateLinkServiceVisibility** проверяет, отображается ли личная служба ссылок для текущего использования.</span><span class="sxs-lookup"><span data-stu-id="be331-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="be331-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be331-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be331-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be331-105">DESCRIPTION</span></span>
<span data-ttu-id="be331-106">Проверьте, отображается ли личная служба ссылок для текущего использования.</span><span class="sxs-lookup"><span data-stu-id="be331-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="be331-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be331-107">EXAMPLES</span></span>

### <span data-ttu-id="be331-108">Пример 1. Проверьте, contoso.cloudapp.azure.com ли contoso.cloudapp.azure.com можно использовать.</span><span class="sxs-lookup"><span data-stu-id="be331-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="be331-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be331-109">PARAMETERS</span></span>

### <span data-ttu-id="be331-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be331-110">-DefaultProfile</span></span>
<span data-ttu-id="be331-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be331-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be331-112">-Location</span><span class="sxs-lookup"><span data-stu-id="be331-112">-Location</span></span>
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

### <span data-ttu-id="be331-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="be331-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="be331-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be331-114">-ResourceGroupName</span></span>
<span data-ttu-id="be331-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be331-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="be331-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be331-116">CommonParameters</span></span>
<span data-ttu-id="be331-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be331-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be331-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be331-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be331-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be331-119">INPUTS</span></span>

### <span data-ttu-id="be331-120">Нет</span><span class="sxs-lookup"><span data-stu-id="be331-120">None</span></span>

## <span data-ttu-id="be331-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be331-121">OUTPUTS</span></span>

### <span data-ttu-id="be331-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be331-122">System.Boolean</span></span>

## <span data-ttu-id="be331-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be331-123">NOTES</span></span>

## <span data-ttu-id="be331-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be331-124">RELATED LINKS</span></span>
