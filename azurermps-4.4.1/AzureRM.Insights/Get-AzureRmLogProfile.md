---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: 2964b95dcaba44ba57d354951eb5ccfb4ea9ef6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733730"
---
# <span data-ttu-id="ce10c-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ce10c-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="ce10c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce10c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce10c-103">Получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="ce10c-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce10c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce10c-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce10c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce10c-105">DESCRIPTION</span></span>
<span data-ttu-id="ce10c-106">Командлет **Get-AzureRmLogProfile** получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="ce10c-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="ce10c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce10c-107">EXAMPLES</span></span>

## <span data-ttu-id="ce10c-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce10c-108">PARAMETERS</span></span>

### <span data-ttu-id="ce10c-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce10c-109">-Name</span></span>
<span data-ttu-id="ce10c-110">Указывает имя профиля, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ce10c-110">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="ce10c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce10c-111">-DefaultProfile</span></span>
<span data-ttu-id="ce10c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce10c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce10c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce10c-113">CommonParameters</span></span>
<span data-ttu-id="ce10c-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce10c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce10c-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce10c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce10c-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce10c-116">INPUTS</span></span>

## <span data-ttu-id="ce10c-117">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce10c-117">OUTPUTS</span></span>

### <span data-ttu-id="ce10c-118">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="ce10c-118">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="ce10c-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce10c-119">NOTES</span></span>

## <span data-ttu-id="ce10c-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce10c-120">RELATED LINKS</span></span>

[<span data-ttu-id="ce10c-121">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ce10c-121">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="ce10c-122">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ce10c-122">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


