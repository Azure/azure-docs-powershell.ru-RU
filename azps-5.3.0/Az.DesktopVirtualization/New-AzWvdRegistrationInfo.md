---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 3e4553fa3d11c8084f103f6e5c6b3f0c57cdb50c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426356"
---
# <span data-ttu-id="de6b4-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="de6b4-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="de6b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="de6b4-103">Создайте сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="de6b4-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="de6b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="de6b4-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de6b4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de6b4-105">DESCRIPTION</span></span>
<span data-ttu-id="de6b4-106">Создайте сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="de6b4-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="de6b4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="de6b4-107">EXAMPLES</span></span>

### <span data-ttu-id="de6b4-108">Пример 1. Создание маркера регистрации виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="de6b4-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="de6b4-109">Эта команда создает маркер регистрации виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="de6b4-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="de6b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de6b4-110">PARAMETERS</span></span>

### <span data-ttu-id="de6b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6b4-111">-DefaultProfile</span></span>
<span data-ttu-id="de6b4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de6b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de6b4-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="de6b4-113">-ExpirationTime</span></span>
<span data-ttu-id="de6b4-114">Срок действия</span><span class="sxs-lookup"><span data-stu-id="de6b4-114">Expiration Time</span></span>

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

### <span data-ttu-id="de6b4-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="de6b4-115">-HostPoolName</span></span>
<span data-ttu-id="de6b4-116">Host Pool Name</span><span class="sxs-lookup"><span data-stu-id="de6b4-116">Host Pool Name</span></span>

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

### <span data-ttu-id="de6b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="de6b4-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="de6b4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="de6b4-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de6b4-119">-SubscriptionId</span></span>
<span data-ttu-id="de6b4-120">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="de6b4-120">Subscription Id</span></span>

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

### <span data-ttu-id="de6b4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de6b4-121">-Confirm</span></span>
<span data-ttu-id="de6b4-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de6b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de6b4-123">-WhatIf</span></span>
<span data-ttu-id="de6b4-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de6b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de6b4-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="de6b4-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6b4-126">CommonParameters</span></span>
<span data-ttu-id="de6b4-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de6b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6b4-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de6b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6b4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de6b4-129">INPUTS</span></span>

## <span data-ttu-id="de6b4-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de6b4-130">OUTPUTS</span></span>

### <span data-ttu-id="de6b4-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="de6b4-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="de6b4-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="de6b4-132">NOTES</span></span>

<span data-ttu-id="de6b4-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="de6b4-133">ALIASES</span></span>

## <span data-ttu-id="de6b4-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de6b4-134">RELATED LINKS</span></span>

