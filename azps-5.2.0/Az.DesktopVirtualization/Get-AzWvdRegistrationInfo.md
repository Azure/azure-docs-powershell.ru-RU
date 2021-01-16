---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 33e0b68e70cb65eee4e9e3178745645aafeb9f9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391724"
---
# <span data-ttu-id="f4b70-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f4b70-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="f4b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4b70-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b70-103">Получите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="f4b70-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f4b70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4b70-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4b70-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b70-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b70-106">Получите сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="f4b70-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="f4b70-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4b70-107">EXAMPLES</span></span>

### <span data-ttu-id="f4b70-108">Пример 1. Получить маркер регистрации виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="f4b70-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="f4b70-109">Эта команда получает маркер регистрации виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="f4b70-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="f4b70-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4b70-110">PARAMETERS</span></span>

### <span data-ttu-id="f4b70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b70-111">-DefaultProfile</span></span>
<span data-ttu-id="f4b70-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b70-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b70-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f4b70-113">-HostPoolName</span></span>
<span data-ttu-id="f4b70-114">Host Pool Name</span><span class="sxs-lookup"><span data-stu-id="f4b70-114">Host Pool Name</span></span>

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

### <span data-ttu-id="f4b70-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b70-115">-ResourceGroupName</span></span>
<span data-ttu-id="f4b70-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f4b70-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f4b70-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4b70-117">-SubscriptionId</span></span>
<span data-ttu-id="f4b70-118">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="f4b70-118">Subscription Id</span></span>

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

### <span data-ttu-id="f4b70-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b70-119">CommonParameters</span></span>
<span data-ttu-id="f4b70-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b70-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b70-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4b70-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b70-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4b70-122">INPUTS</span></span>

## <span data-ttu-id="f4b70-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4b70-123">OUTPUTS</span></span>

### <span data-ttu-id="f4b70-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="f4b70-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.RegistrationInfo</span></span>

## <span data-ttu-id="f4b70-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4b70-125">NOTES</span></span>

<span data-ttu-id="f4b70-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f4b70-126">ALIASES</span></span>

## <span data-ttu-id="f4b70-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4b70-127">RELATED LINKS</span></span>

