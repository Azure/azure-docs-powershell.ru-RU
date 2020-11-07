---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732714"
---
# <span data-ttu-id="00f6c-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="00f6c-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="00f6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="00f6c-103">Получение клавиш доступа к службе сигнальных служб.</span><span class="sxs-lookup"><span data-stu-id="00f6c-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00f6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00f6c-104">SYNTAX</span></span>

### <span data-ttu-id="00f6c-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00f6c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00f6c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00f6c-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00f6c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00f6c-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00f6c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00f6c-108">DESCRIPTION</span></span>
<span data-ttu-id="00f6c-109">Получение клавиш доступа к службе сигнальных служб.</span><span class="sxs-lookup"><span data-stu-id="00f6c-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="00f6c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00f6c-110">EXAMPLES</span></span>

### <span data-ttu-id="00f6c-111">Получение клавиш доступа к определенному сигнальному службе</span><span class="sxs-lookup"><span data-stu-id="00f6c-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="00f6c-112">Получение клавиш доступа из объекта обслуживания SignalR в канале</span><span class="sxs-lookup"><span data-stu-id="00f6c-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="00f6c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00f6c-113">PARAMETERS</span></span>

### <span data-ttu-id="00f6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f6c-114">-DefaultProfile</span></span>
<span data-ttu-id="00f6c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00f6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f6c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00f6c-116">-InputObject</span></span>
<span data-ttu-id="00f6c-117">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="00f6c-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00f6c-118">-Name</span></span>
<span data-ttu-id="00f6c-119">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="00f6c-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="00f6c-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="00f6c-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00f6c-122">-ResourceId</span></span>
<span data-ttu-id="00f6c-123">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="00f6c-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f6c-124">CommonParameters</span></span>
<span data-ttu-id="00f6c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00f6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f6c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f6c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f6c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00f6c-127">INPUTS</span></span>

### <span data-ttu-id="00f6c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00f6c-128">System.String</span></span>
<span data-ttu-id="00f6c-129">Параметры: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00f6c-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="00f6c-130">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="00f6c-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="00f6c-131">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00f6c-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="00f6c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00f6c-132">OUTPUTS</span></span>

### <span data-ttu-id="00f6c-133">Microsoft. Azure. Commands. SignalR. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="00f6c-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="00f6c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="00f6c-134">NOTES</span></span>

## <span data-ttu-id="00f6c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00f6c-135">RELATED LINKS</span></span>
