---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326441"
---
# <span data-ttu-id="2f8c9-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="2f8c9-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="2f8c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8c9-103">Создайте объект PSBackendPoolsSetting для создания передней двери.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="2f8c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f8c9-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f8c9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f8c9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f8c9-106">С **новым объектом PSBackendPoolsSettingObject в AzFrontDoorBackendpoolsObject** создается объект PSBackendPoolsSettings для создания передней двери.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="2f8c9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f8c9-107">EXAMPLES</span></span>

### <span data-ttu-id="2f8c9-108">Пример 1. Создание объекта BackendPoolsSettings с использованием по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2f8c9-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="2f8c9-109">Пример 2. Создание объекта BackendPoolsSettings с указанными пользователем значениями</span><span class="sxs-lookup"><span data-stu-id="2f8c9-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="2f8c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f8c9-110">PARAMETERS</span></span>

### <span data-ttu-id="2f8c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8c9-111">-DefaultProfile</span></span>
<span data-ttu-id="2f8c9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f8c9-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="2f8c9-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="2f8c9-114">Нужно ли принудительно проверять имена сертификатов по HTTPS-запросам во все пулы backend.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="2f8c9-115">Никакие действия с запросами, не относясьми к HTTPS-запросам.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-115">No effect on non-HTTPS requests.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f8c9-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2f8c9-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="2f8c9-117">Отправка и получение времени отправки запроса на переадружение на дополнительный отправитель.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="2f8c9-118">После этого запрос не справился с запросом и возвращает его.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-118">When timeout is reached, the request fails and returns.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f8c9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8c9-119">CommonParameters</span></span>
<span data-ttu-id="2f8c9-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8c9-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f8c9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8c9-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f8c9-122">INPUTS</span></span>

### <span data-ttu-id="2f8c9-123">Нет</span><span class="sxs-lookup"><span data-stu-id="2f8c9-123">None</span></span>

## <span data-ttu-id="2f8c9-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f8c9-124">OUTPUTS</span></span>

### <span data-ttu-id="2f8c9-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="2f8c9-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="2f8c9-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f8c9-126">NOTES</span></span>

## <span data-ttu-id="2f8c9-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f8c9-127">RELATED LINKS</span></span>
