---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: e05ea63bddc8dc61332a31e4fa44aa1b7428055a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904282"
---
# <span data-ttu-id="cb438-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="cb438-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="cb438-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb438-102">SYNOPSIS</span></span>
<span data-ttu-id="cb438-103">**Тест-AzPrivateLinkServiceVisibility** проверяет, является ли служба частной ссылки видимой для текущего использования.</span><span class="sxs-lookup"><span data-stu-id="cb438-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="cb438-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb438-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb438-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb438-105">DESCRIPTION</span></span>
<span data-ttu-id="cb438-106">Проверьте, является ли служба частной ссылки видимой для текущего использования.</span><span class="sxs-lookup"><span data-stu-id="cb438-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="cb438-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb438-107">EXAMPLES</span></span>

### <span data-ttu-id="cb438-108">Пример 1: Проверка доступности contoso.cloudapp.azure.com для использования.</span><span class="sxs-lookup"><span data-stu-id="cb438-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="cb438-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb438-109">PARAMETERS</span></span>

### <span data-ttu-id="cb438-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb438-110">-DefaultProfile</span></span>
<span data-ttu-id="cb438-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb438-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb438-112">-Location</span><span class="sxs-lookup"><span data-stu-id="cb438-112">-Location</span></span>
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

### <span data-ttu-id="cb438-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="cb438-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="cb438-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb438-114">-ResourceGroupName</span></span>
<span data-ttu-id="cb438-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb438-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cb438-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb438-116">CommonParameters</span></span>
<span data-ttu-id="cb438-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb438-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb438-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb438-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb438-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb438-119">INPUTS</span></span>

### <span data-ttu-id="cb438-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="cb438-120">None</span></span>

## <span data-ttu-id="cb438-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb438-121">OUTPUTS</span></span>

### <span data-ttu-id="cb438-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb438-122">System.Boolean</span></span>

## <span data-ttu-id="cb438-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb438-123">NOTES</span></span>

## <span data-ttu-id="cb438-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb438-124">RELATED LINKS</span></span>
