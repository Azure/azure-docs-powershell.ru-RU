---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247313"
---
# <span data-ttu-id="09c29-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="09c29-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="09c29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09c29-102">SYNOPSIS</span></span>
<span data-ttu-id="09c29-103">Получение ключей учетной записи удаленной отрисовки</span><span class="sxs-lookup"><span data-stu-id="09c29-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="09c29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09c29-104">SYNTAX</span></span>

### <span data-ttu-id="09c29-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09c29-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09c29-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09c29-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09c29-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="09c29-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09c29-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09c29-108">DESCRIPTION</span></span>
<span data-ttu-id="09c29-109">Получение ключей разработчика для учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="09c29-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="09c29-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09c29-110">EXAMPLES</span></span>

### <span data-ttu-id="09c29-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09c29-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="09c29-112">Получение ключей разработчика учетной записи удаленной отрисовки "example" из текущей подписки и группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="09c29-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="09c29-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="09c29-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="09c29-114">Получение ключей разработчика учетной записи удаленной отрисовки "пример" из текущей подписки и группы ресурсов "Rg1" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="09c29-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="09c29-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09c29-115">PARAMETERS</span></span>

### <span data-ttu-id="09c29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c29-116">-DefaultProfile</span></span>
<span data-ttu-id="09c29-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09c29-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09c29-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09c29-118">-InputObject</span></span>
<span data-ttu-id="09c29-119">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="09c29-119">The custom domain object.</span></span>

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

### <span data-ttu-id="09c29-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09c29-120">-Name</span></span>
<span data-ttu-id="09c29-121">Имя учетной записи для удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="09c29-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="09c29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c29-122">-ResourceGroupName</span></span>
<span data-ttu-id="09c29-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09c29-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="09c29-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09c29-124">-ResourceId</span></span>
<span data-ttu-id="09c29-125">Идентификатор ресурса для учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="09c29-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="09c29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c29-126">CommonParameters</span></span>
<span data-ttu-id="09c29-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09c29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="09c29-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c29-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c29-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09c29-129">INPUTS</span></span>

### <span data-ttu-id="09c29-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09c29-130">System.String</span></span>

### <span data-ttu-id="09c29-131">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="09c29-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="09c29-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09c29-132">OUTPUTS</span></span>

### <span data-ttu-id="09c29-133">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="09c29-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="09c29-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="09c29-134">NOTES</span></span>

## <span data-ttu-id="09c29-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09c29-135">RELATED LINKS</span></span>
