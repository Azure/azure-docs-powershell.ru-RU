---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 3e4553fa3d11c8084f103f6e5c6b3f0c57cdb50c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220132"
---
# <span data-ttu-id="81a47-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="81a47-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="81a47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81a47-102">SYNOPSIS</span></span>
<span data-ttu-id="81a47-103">Создайте сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="81a47-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="81a47-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81a47-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81a47-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81a47-105">DESCRIPTION</span></span>
<span data-ttu-id="81a47-106">Создайте сведения о регистрации виртуальных рабочих стола Windows.</span><span class="sxs-lookup"><span data-stu-id="81a47-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="81a47-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81a47-107">EXAMPLES</span></span>

### <span data-ttu-id="81a47-108">Пример 1. Создание маркера регистрации виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="81a47-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="81a47-109">Эта команда создает маркер регистрации виртуального рабочего стола Windows в пуле хостов.</span><span class="sxs-lookup"><span data-stu-id="81a47-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="81a47-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81a47-110">PARAMETERS</span></span>

### <span data-ttu-id="81a47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a47-111">-DefaultProfile</span></span>
<span data-ttu-id="81a47-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81a47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81a47-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="81a47-113">-ExpirationTime</span></span>
<span data-ttu-id="81a47-114">Срок действия</span><span class="sxs-lookup"><span data-stu-id="81a47-114">Expiration Time</span></span>

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

### <span data-ttu-id="81a47-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="81a47-115">-HostPoolName</span></span>
<span data-ttu-id="81a47-116">Host Pool Name</span><span class="sxs-lookup"><span data-stu-id="81a47-116">Host Pool Name</span></span>

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

### <span data-ttu-id="81a47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a47-117">-ResourceGroupName</span></span>
<span data-ttu-id="81a47-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="81a47-118">Resource Group Name</span></span>

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

### <span data-ttu-id="81a47-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81a47-119">-SubscriptionId</span></span>
<span data-ttu-id="81a47-120">ИД подписки</span><span class="sxs-lookup"><span data-stu-id="81a47-120">Subscription Id</span></span>

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

### <span data-ttu-id="81a47-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81a47-121">-Confirm</span></span>
<span data-ttu-id="81a47-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a47-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a47-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a47-123">-WhatIf</span></span>
<span data-ttu-id="81a47-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a47-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81a47-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="81a47-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a47-126">CommonParameters</span></span>
<span data-ttu-id="81a47-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a47-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81a47-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a47-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81a47-129">INPUTS</span></span>

## <span data-ttu-id="81a47-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81a47-130">OUTPUTS</span></span>

### <span data-ttu-id="81a47-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="81a47-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="81a47-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81a47-132">NOTES</span></span>

<span data-ttu-id="81a47-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="81a47-133">ALIASES</span></span>

## <span data-ttu-id="81a47-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81a47-134">RELATED LINKS</span></span>

