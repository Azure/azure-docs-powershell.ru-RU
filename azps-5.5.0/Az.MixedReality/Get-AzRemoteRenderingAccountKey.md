---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228161"
---
# <span data-ttu-id="41f6e-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="41f6e-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="41f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="41f6e-103">Получить ключи от учетной записи удаленной отрисовки</span><span class="sxs-lookup"><span data-stu-id="41f6e-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="41f6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41f6e-104">SYNTAX</span></span>

### <span data-ttu-id="41f6e-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41f6e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41f6e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41f6e-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41f6e-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="41f6e-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41f6e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41f6e-108">DESCRIPTION</span></span>
<span data-ttu-id="41f6e-109">Получите ключи разработчика для учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="41f6e-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="41f6e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41f6e-110">EXAMPLES</span></span>

### <span data-ttu-id="41f6e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41f6e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="41f6e-112">Получите ключи разработчика для удаленной отрисовки "example" из текущей подписки и группы ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="41f6e-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="41f6e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="41f6e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="41f6e-114">Получите ключи разработчика "example" учетной записи удаленной отрисовки из текущей подписки и группы ресурсов "rg1" с piping.</span><span class="sxs-lookup"><span data-stu-id="41f6e-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="41f6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41f6e-115">PARAMETERS</span></span>

### <span data-ttu-id="41f6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f6e-116">-DefaultProfile</span></span>
<span data-ttu-id="41f6e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41f6e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f6e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41f6e-118">-InputObject</span></span>
<span data-ttu-id="41f6e-119">Объект настраиваемного домена.</span><span class="sxs-lookup"><span data-stu-id="41f6e-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41f6e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="41f6e-120">-Name</span></span>
<span data-ttu-id="41f6e-121">Имя учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="41f6e-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f6e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f6e-122">-ResourceGroupName</span></span>
<span data-ttu-id="41f6e-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41f6e-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f6e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41f6e-124">-ResourceId</span></span>
<span data-ttu-id="41f6e-125">ИД ресурса учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="41f6e-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f6e-126">CommonParameters</span></span>
<span data-ttu-id="41f6e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="41f6e-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f6e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f6e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41f6e-129">INPUTS</span></span>

### <span data-ttu-id="41f6e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="41f6e-130">System.String</span></span>

### <span data-ttu-id="41f6e-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="41f6e-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="41f6e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41f6e-132">OUTPUTS</span></span>

### <span data-ttu-id="41f6e-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="41f6e-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="41f6e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41f6e-134">NOTES</span></span>

## <span data-ttu-id="41f6e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41f6e-135">RELATED LINKS</span></span>
