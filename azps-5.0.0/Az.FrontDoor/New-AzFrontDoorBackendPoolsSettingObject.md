---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247423"
---
# <span data-ttu-id="abb54-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="abb54-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="abb54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abb54-102">SYNOPSIS</span></span>
<span data-ttu-id="abb54-103">Создайте объект PSBackendPoolsSetting для создания передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="abb54-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="abb54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abb54-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb54-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abb54-105">DESCRIPTION</span></span>
<span data-ttu-id="abb54-106">Командлет **New-AzFrontDoorBackendpoolsSettingObject** создает новый объект PSBackendPoolsSettings для создания передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="abb54-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="abb54-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abb54-107">EXAMPLES</span></span>

### <span data-ttu-id="abb54-108">Пример 1: создание объекта BackendPoolsSettings с помощью значений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="abb54-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="abb54-109">Пример 2: создание объекта BackendPoolsSettings с указанными пользователем значениями</span><span class="sxs-lookup"><span data-stu-id="abb54-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="abb54-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abb54-110">PARAMETERS</span></span>

### <span data-ttu-id="abb54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb54-111">-DefaultProfile</span></span>
<span data-ttu-id="abb54-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abb54-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abb54-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="abb54-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="abb54-114">Следует ли применять проверку имени сертификата для запросов HTTPS ко всем пулам баз данных.</span><span class="sxs-lookup"><span data-stu-id="abb54-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="abb54-115">Не влияет на запросы, не относящиеся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="abb54-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="abb54-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="abb54-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="abb54-117">Отправка и получение таймаута для запроса на переадресацию на сервер.</span><span class="sxs-lookup"><span data-stu-id="abb54-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="abb54-118">При достижении тайм-аута запрос завершается сбоем и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="abb54-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="abb54-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb54-119">CommonParameters</span></span>
<span data-ttu-id="abb54-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abb54-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb54-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abb54-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb54-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abb54-122">INPUTS</span></span>

### <span data-ttu-id="abb54-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="abb54-123">None</span></span>

## <span data-ttu-id="abb54-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abb54-124">OUTPUTS</span></span>

### <span data-ttu-id="abb54-125">Microsoft. Azure. Commands. FrontDoor. Models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="abb54-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="abb54-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="abb54-126">NOTES</span></span>

## <span data-ttu-id="abb54-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abb54-127">RELATED LINKS</span></span>