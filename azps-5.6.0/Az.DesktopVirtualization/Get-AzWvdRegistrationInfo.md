---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 868cbf6aaaf9b9c304c6afa65e63e6eca12910d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962035"
---
# <span data-ttu-id="78ea7-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="78ea7-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="78ea7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="78ea7-103">Получите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="78ea7-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="78ea7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78ea7-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="78ea7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="78ea7-106">Получите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="78ea7-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="78ea7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="78ea7-108">Пример 1. Получить маркер регистрации виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="78ea7-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="78ea7-109">Эта команда получает маркер регистрации виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="78ea7-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="78ea7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="78ea7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ea7-111">-DefaultProfile</span></span>
<span data-ttu-id="78ea7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78ea7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78ea7-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="78ea7-113">-HostPoolName</span></span>
<span data-ttu-id="78ea7-114">Host Pool Name</span><span class="sxs-lookup"><span data-stu-id="78ea7-114">Host Pool Name</span></span>

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

### <span data-ttu-id="78ea7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ea7-115">-ResourceGroupName</span></span>
<span data-ttu-id="78ea7-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="78ea7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="78ea7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78ea7-117">-SubscriptionId</span></span>
<span data-ttu-id="78ea7-118">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="78ea7-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78ea7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ea7-119">CommonParameters</span></span>
<span data-ttu-id="78ea7-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ea7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ea7-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78ea7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ea7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78ea7-122">INPUTS</span></span>

## <span data-ttu-id="78ea7-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78ea7-123">OUTPUTS</span></span>

### <span data-ttu-id="78ea7-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="78ea7-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="78ea7-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78ea7-125">NOTES</span></span>

<span data-ttu-id="78ea7-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="78ea7-126">ALIASES</span></span>

## <span data-ttu-id="78ea7-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78ea7-127">RELATED LINKS</span></span>

