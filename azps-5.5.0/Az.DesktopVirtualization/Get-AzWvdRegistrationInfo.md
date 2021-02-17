---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 52b2d636e9ab4dbde9cbafc69da3122828a91477
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234572"
---
# <span data-ttu-id="f4f71-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f4f71-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="f4f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f71-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f71-103">Получите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="f4f71-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f4f71-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4f71-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4f71-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4f71-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f71-106">Получите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="f4f71-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f4f71-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4f71-107">EXAMPLES</span></span>

### <span data-ttu-id="f4f71-108">Пример 1. Получить маркер регистрации виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="f4f71-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="f4f71-109">Эта команда получает маркер регистрации виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="f4f71-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="f4f71-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4f71-110">PARAMETERS</span></span>

### <span data-ttu-id="f4f71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f71-111">-DefaultProfile</span></span>
<span data-ttu-id="f4f71-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f71-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f71-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f4f71-113">-HostPoolName</span></span>
<span data-ttu-id="f4f71-114">Host Pool Name</span><span class="sxs-lookup"><span data-stu-id="f4f71-114">Host Pool Name</span></span>

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

### <span data-ttu-id="f4f71-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f71-115">-ResourceGroupName</span></span>
<span data-ttu-id="f4f71-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f4f71-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f4f71-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4f71-117">-SubscriptionId</span></span>
<span data-ttu-id="f4f71-118">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="f4f71-118">Subscription Id</span></span>

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

### <span data-ttu-id="f4f71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f71-119">CommonParameters</span></span>
<span data-ttu-id="f4f71-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f71-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4f71-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f71-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4f71-122">INPUTS</span></span>

## <span data-ttu-id="f4f71-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4f71-123">OUTPUTS</span></span>

### <span data-ttu-id="f4f71-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f4f71-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="f4f71-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4f71-125">NOTES</span></span>

<span data-ttu-id="f4f71-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f4f71-126">ALIASES</span></span>

## <span data-ttu-id="f4f71-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4f71-127">RELATED LINKS</span></span>

