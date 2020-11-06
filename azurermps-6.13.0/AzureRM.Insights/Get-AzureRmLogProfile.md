---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568914"
---
# <span data-ttu-id="e7e48-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e7e48-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="e7e48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7e48-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e48-103">Получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="e7e48-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7e48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7e48-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7e48-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e48-106">Командлет **Get-AzureRmLogProfile** получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="e7e48-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="e7e48-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7e48-107">EXAMPLES</span></span>

## <span data-ttu-id="e7e48-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7e48-108">PARAMETERS</span></span>

### <span data-ttu-id="e7e48-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e48-109">-DefaultProfile</span></span>
<span data-ttu-id="e7e48-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7e48-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7e48-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7e48-111">-Name</span></span>
<span data-ttu-id="e7e48-112">Указывает имя профиля, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e7e48-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="e7e48-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e48-113">CommonParameters</span></span>
<span data-ttu-id="e7e48-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7e48-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e48-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7e48-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e48-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7e48-116">INPUTS</span></span>

### <span data-ttu-id="e7e48-117">System. String</span><span class="sxs-lookup"><span data-stu-id="e7e48-117">System.String</span></span>

## <span data-ttu-id="e7e48-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7e48-118">OUTPUTS</span></span>

### <span data-ttu-id="e7e48-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="e7e48-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="e7e48-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7e48-120">NOTES</span></span>

## <span data-ttu-id="e7e48-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7e48-121">RELATED LINKS</span></span>

[<span data-ttu-id="e7e48-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e7e48-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="e7e48-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e7e48-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


