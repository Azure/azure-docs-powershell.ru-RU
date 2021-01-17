---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395180"
---
# <span data-ttu-id="f9221-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="f9221-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="f9221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9221-102">SYNOPSIS</span></span>
<span data-ttu-id="f9221-103">Создает контакт в памяти для peerAsn.</span><span class="sxs-lookup"><span data-stu-id="f9221-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="f9221-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f9221-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9221-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9221-105">DESCRIPTION</span></span>
<span data-ttu-id="f9221-106">Создайте в памяти информацию о контакте PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="f9221-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="f9221-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f9221-107">EXAMPLES</span></span>

### <span data-ttu-id="f9221-108">Создание подробных контактов и добавление в peerAsn</span><span class="sxs-lookup"><span data-stu-id="f9221-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="f9221-109">Роль и электронная почта требуются.</span><span class="sxs-lookup"><span data-stu-id="f9221-109">Role and email are required.</span></span> <span data-ttu-id="f9221-110">Телефон не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f9221-110">Phone is optional.</span></span> <span data-ttu-id="f9221-111">Телефон поддерживает +-() или пробелы.</span><span class="sxs-lookup"><span data-stu-id="f9221-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="f9221-112">Одноранговая связь должна включать по крайней мере один контакт с типом "Noc"</span><span class="sxs-lookup"><span data-stu-id="f9221-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="f9221-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9221-113">PARAMETERS</span></span>

### <span data-ttu-id="f9221-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9221-114">-DefaultProfile</span></span>
<span data-ttu-id="f9221-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9221-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9221-116">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="f9221-116">-Email</span></span>
<span data-ttu-id="f9221-117">Адреса электронной почты, используемые для связи, если проблемы обычно заданы в Центре сетевых операций</span><span class="sxs-lookup"><span data-stu-id="f9221-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="f9221-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="f9221-118">-Phone</span></span>
<span data-ttu-id="f9221-119">Телефон, используемый для связи, если проблемы обычно заданы в Центре сетевых операций</span><span class="sxs-lookup"><span data-stu-id="f9221-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9221-120">-Роль</span><span class="sxs-lookup"><span data-stu-id="f9221-120">-Role</span></span>
<span data-ttu-id="f9221-121">Выберите роль, которая лучше всего подходит для контактных данных.</span><span class="sxs-lookup"><span data-stu-id="f9221-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="f9221-122">NoC Contact является обязательной.</span><span class="sxs-lookup"><span data-stu-id="f9221-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="f9221-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9221-123">CommonParameters</span></span>
<span data-ttu-id="f9221-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9221-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9221-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9221-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9221-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9221-126">INPUTS</span></span>

### <span data-ttu-id="f9221-127">Нет</span><span class="sxs-lookup"><span data-stu-id="f9221-127">None</span></span>

## <span data-ttu-id="f9221-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f9221-128">OUTPUTS</span></span>

### <span data-ttu-id="f9221-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="f9221-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="f9221-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f9221-130">NOTES</span></span>

## <span data-ttu-id="f9221-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9221-131">RELATED LINKS</span></span>
