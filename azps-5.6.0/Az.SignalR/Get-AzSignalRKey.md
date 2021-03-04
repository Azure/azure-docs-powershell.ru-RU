---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: 5bcec1e6843c2f68a6d0f602bdc9b991d5fcacdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955496"
---
# <span data-ttu-id="5a49b-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="5a49b-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="5a49b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a49b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a49b-103">Получите ключи доступа службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="5a49b-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="5a49b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a49b-104">SYNTAX</span></span>

### <span data-ttu-id="5a49b-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a49b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a49b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a49b-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a49b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a49b-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a49b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a49b-108">DESCRIPTION</span></span>
<span data-ttu-id="5a49b-109">Получите ключи доступа службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="5a49b-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="5a49b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a49b-110">EXAMPLES</span></span>

### <span data-ttu-id="5a49b-111">Получить ключи доступа для определенной службы SignalR</span><span class="sxs-lookup"><span data-stu-id="5a49b-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="5a49b-112">Помиминай клавиши доступа от объекта службы SignalR в трубе</span><span class="sxs-lookup"><span data-stu-id="5a49b-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="5a49b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a49b-113">PARAMETERS</span></span>

### <span data-ttu-id="5a49b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a49b-114">-DefaultProfile</span></span>
<span data-ttu-id="5a49b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a49b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a49b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a49b-116">-InputObject</span></span>
<span data-ttu-id="5a49b-117">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="5a49b-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5a49b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5a49b-118">-Name</span></span>
<span data-ttu-id="5a49b-119">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="5a49b-119">SignalR service name.</span></span>

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

### <span data-ttu-id="5a49b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a49b-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a49b-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a49b-121">Resource group name.</span></span>

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

### <span data-ttu-id="5a49b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a49b-122">-ResourceId</span></span>
<span data-ttu-id="5a49b-123">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="5a49b-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5a49b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a49b-124">CommonParameters</span></span>
<span data-ttu-id="5a49b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a49b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a49b-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a49b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a49b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a49b-127">INPUTS</span></span>

### <span data-ttu-id="5a49b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5a49b-128">System.String</span></span>
### <span data-ttu-id="5a49b-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="5a49b-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="5a49b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a49b-130">OUTPUTS</span></span>

### <span data-ttu-id="5a49b-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="5a49b-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="5a49b-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a49b-132">NOTES</span></span>

## <span data-ttu-id="5a49b-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a49b-133">RELATED LINKS</span></span>
