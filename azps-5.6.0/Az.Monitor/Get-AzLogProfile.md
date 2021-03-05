---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 51dd39f18874fc1888fb37277f5de0557cf3553b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980008"
---
# <span data-ttu-id="f63fd-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f63fd-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="f63fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f63fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f63fd-103">Получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="f63fd-103">Gets a log profile.</span></span>

## <span data-ttu-id="f63fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f63fd-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f63fd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f63fd-105">DESCRIPTION</span></span>
<span data-ttu-id="f63fd-106">Профиль **журнала получает cmdlet Get-AzLogProfile.**</span><span class="sxs-lookup"><span data-stu-id="f63fd-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="f63fd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f63fd-107">EXAMPLES</span></span>

## <span data-ttu-id="f63fd-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f63fd-108">PARAMETERS</span></span>

### <span data-ttu-id="f63fd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63fd-109">-DefaultProfile</span></span>
<span data-ttu-id="f63fd-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f63fd-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f63fd-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f63fd-111">-Name</span></span>
<span data-ttu-id="f63fd-112">Имя профиля журнала, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="f63fd-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="f63fd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63fd-113">CommonParameters</span></span>
<span data-ttu-id="f63fd-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f63fd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63fd-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f63fd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63fd-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f63fd-116">INPUTS</span></span>

### <span data-ttu-id="f63fd-117">System.String</span><span class="sxs-lookup"><span data-stu-id="f63fd-117">System.String</span></span>

## <span data-ttu-id="f63fd-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f63fd-118">OUTPUTS</span></span>

### <span data-ttu-id="f63fd-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="f63fd-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="f63fd-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f63fd-120">NOTES</span></span>

## <span data-ttu-id="f63fd-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f63fd-121">RELATED LINKS</span></span>

[<span data-ttu-id="f63fd-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f63fd-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="f63fd-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f63fd-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


