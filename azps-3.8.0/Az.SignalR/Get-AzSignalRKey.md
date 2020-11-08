---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065259"
---
# <span data-ttu-id="cf565-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="cf565-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="cf565-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf565-102">SYNOPSIS</span></span>
<span data-ttu-id="cf565-103">Получение клавиш доступа к службе сигнальных служб.</span><span class="sxs-lookup"><span data-stu-id="cf565-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="cf565-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf565-104">SYNTAX</span></span>

### <span data-ttu-id="cf565-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf565-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf565-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf565-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf565-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf565-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf565-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf565-108">DESCRIPTION</span></span>
<span data-ttu-id="cf565-109">Получение клавиш доступа к службе сигнальных служб.</span><span class="sxs-lookup"><span data-stu-id="cf565-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="cf565-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf565-110">EXAMPLES</span></span>

### <span data-ttu-id="cf565-111">Получение клавиш доступа к определенному сигнальному службе</span><span class="sxs-lookup"><span data-stu-id="cf565-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="cf565-112">Получение клавиш доступа из объекта обслуживания SignalR в канале</span><span class="sxs-lookup"><span data-stu-id="cf565-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="cf565-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf565-113">PARAMETERS</span></span>

### <span data-ttu-id="cf565-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf565-114">-DefaultProfile</span></span>
<span data-ttu-id="cf565-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf565-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf565-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf565-116">-InputObject</span></span>
<span data-ttu-id="cf565-117">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="cf565-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="cf565-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf565-118">-Name</span></span>
<span data-ttu-id="cf565-119">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="cf565-119">SignalR service name.</span></span>

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

### <span data-ttu-id="cf565-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf565-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf565-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf565-121">Resource group name.</span></span>

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

### <span data-ttu-id="cf565-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf565-122">-ResourceId</span></span>
<span data-ttu-id="cf565-123">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="cf565-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="cf565-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf565-124">CommonParameters</span></span>
<span data-ttu-id="cf565-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf565-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf565-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf565-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf565-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf565-127">INPUTS</span></span>

### <span data-ttu-id="cf565-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cf565-128">System.String</span></span>
### <span data-ttu-id="cf565-129">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="cf565-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="cf565-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf565-130">OUTPUTS</span></span>

### <span data-ttu-id="cf565-131">Microsoft. Azure. Commands. SignalR. Models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="cf565-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="cf565-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf565-132">NOTES</span></span>

## <span data-ttu-id="cf565-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf565-133">RELATED LINKS</span></span>
