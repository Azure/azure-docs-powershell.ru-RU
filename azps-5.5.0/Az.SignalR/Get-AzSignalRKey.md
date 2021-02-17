---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223108"
---
# <span data-ttu-id="56af4-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="56af4-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="56af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56af4-102">SYNOPSIS</span></span>
<span data-ttu-id="56af4-103">Получите ключи доступа службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="56af4-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="56af4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56af4-104">SYNTAX</span></span>

### <span data-ttu-id="56af4-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56af4-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56af4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56af4-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56af4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56af4-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56af4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56af4-108">DESCRIPTION</span></span>
<span data-ttu-id="56af4-109">Получите ключи доступа службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="56af4-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="56af4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56af4-110">EXAMPLES</span></span>

### <span data-ttu-id="56af4-111">Получить ключи доступа для определенной службы SignalR</span><span class="sxs-lookup"><span data-stu-id="56af4-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="56af4-112">Помиминай клавиши доступа от объекта службы SignalR в трубе</span><span class="sxs-lookup"><span data-stu-id="56af4-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="56af4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56af4-113">PARAMETERS</span></span>

### <span data-ttu-id="56af4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56af4-114">-DefaultProfile</span></span>
<span data-ttu-id="56af4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56af4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56af4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56af4-116">-InputObject</span></span>
<span data-ttu-id="56af4-117">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="56af4-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="56af4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56af4-118">-Name</span></span>
<span data-ttu-id="56af4-119">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="56af4-119">SignalR service name.</span></span>

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

### <span data-ttu-id="56af4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56af4-120">-ResourceGroupName</span></span>
<span data-ttu-id="56af4-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56af4-121">Resource group name.</span></span>

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

### <span data-ttu-id="56af4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56af4-122">-ResourceId</span></span>
<span data-ttu-id="56af4-123">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="56af4-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="56af4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56af4-124">CommonParameters</span></span>
<span data-ttu-id="56af4-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56af4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56af4-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56af4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56af4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56af4-127">INPUTS</span></span>

### <span data-ttu-id="56af4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="56af4-128">System.String</span></span>
### <span data-ttu-id="56af4-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="56af4-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="56af4-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56af4-130">OUTPUTS</span></span>

### <span data-ttu-id="56af4-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="56af4-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="56af4-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56af4-132">NOTES</span></span>

## <span data-ttu-id="56af4-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56af4-133">RELATED LINKS</span></span>
