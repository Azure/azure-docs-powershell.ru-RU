---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078318"
---
# <span data-ttu-id="5c2bd-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="5c2bd-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="5c2bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2bd-103">Получение сведений о регистрации виртуальных рабочих столов в Windows.</span><span class="sxs-lookup"><span data-stu-id="5c2bd-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="5c2bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c2bd-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5c2bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c2bd-105">DESCRIPTION</span></span>
<span data-ttu-id="5c2bd-106">Получение сведений о регистрации виртуальных рабочих столов в Windows.</span><span class="sxs-lookup"><span data-stu-id="5c2bd-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="5c2bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c2bd-107">EXAMPLES</span></span>

### <span data-ttu-id="5c2bd-108">Пример 1: получение маркера регистрации виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="5c2bd-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="5c2bd-109">Эта команда получает маркер регистрации виртуальных рабочих столов Windows в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="5c2bd-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="5c2bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c2bd-110">PARAMETERS</span></span>

### <span data-ttu-id="5c2bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2bd-111">-DefaultProfile</span></span>
<span data-ttu-id="5c2bd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c2bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2bd-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5c2bd-113">-HostPoolName</span></span>
<span data-ttu-id="5c2bd-114">Имя пула узлов</span><span class="sxs-lookup"><span data-stu-id="5c2bd-114">Host Pool Name</span></span>

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

### <span data-ttu-id="5c2bd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2bd-115">-ResourceGroupName</span></span>
<span data-ttu-id="5c2bd-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5c2bd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="5c2bd-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c2bd-117">-SubscriptionId</span></span>
<span data-ttu-id="5c2bd-118">Идентификатор подписки</span><span class="sxs-lookup"><span data-stu-id="5c2bd-118">Subscription Id</span></span>

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

### <span data-ttu-id="5c2bd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2bd-119">CommonParameters</span></span>
<span data-ttu-id="5c2bd-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c2bd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2bd-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c2bd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2bd-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c2bd-122">INPUTS</span></span>

## <span data-ttu-id="5c2bd-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c2bd-123">OUTPUTS</span></span>

### <span data-ttu-id="5c2bd-124">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="5c2bd-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="5c2bd-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c2bd-125">NOTES</span></span>

<span data-ttu-id="5c2bd-126">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5c2bd-126">ALIASES</span></span>

## <span data-ttu-id="5c2bd-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c2bd-127">RELATED LINKS</span></span>

