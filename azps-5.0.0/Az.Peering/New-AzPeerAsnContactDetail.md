---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246369"
---
# <span data-ttu-id="c4c73-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="c4c73-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="c4c73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4c73-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c73-103">Создание сведений о контакте в памяти для PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="c4c73-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="c4c73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4c73-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4c73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4c73-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c73-106">Создание PeerAsn контактных данных в памяти.</span><span class="sxs-lookup"><span data-stu-id="c4c73-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="c4c73-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4c73-107">EXAMPLES</span></span>

### <span data-ttu-id="c4c73-108">Создание сведений о контакте и добавление в PeerAsn</span><span class="sxs-lookup"><span data-stu-id="c4c73-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="c4c73-109">Требуется роль и электронная почта.</span><span class="sxs-lookup"><span data-stu-id="c4c73-109">Role and email are required.</span></span> <span data-ttu-id="c4c73-110">Телефонный номер является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c4c73-110">Phone is optional.</span></span> <span data-ttu-id="c4c73-111">Телефон поддерживает +-() или пробелы.</span><span class="sxs-lookup"><span data-stu-id="c4c73-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="c4c73-112">PeerAsn должен содержать по крайней мере один контакт сведения типа "NOC"</span><span class="sxs-lookup"><span data-stu-id="c4c73-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="c4c73-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4c73-113">PARAMETERS</span></span>

### <span data-ttu-id="c4c73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c73-114">-DefaultProfile</span></span>
<span data-ttu-id="c4c73-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c73-116">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="c4c73-116">-Email</span></span>
<span data-ttu-id="c4c73-117">Адреса электронной почты, которые используются для связи, если arrise обычно является центром сетевых операций</span><span class="sxs-lookup"><span data-stu-id="c4c73-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="c4c73-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="c4c73-118">-Phone</span></span>
<span data-ttu-id="c4c73-119">Телефон, используемый для связи в случае проблем arrise обычно является центром сетевых операций</span><span class="sxs-lookup"><span data-stu-id="c4c73-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="c4c73-120">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="c4c73-120">-Role</span></span>
<span data-ttu-id="c4c73-121">Выберите роль, которая лучше всего подходит для контактных данных.</span><span class="sxs-lookup"><span data-stu-id="c4c73-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="c4c73-122">Контакт в службе NOC является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c4c73-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="c4c73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c73-123">CommonParameters</span></span>
<span data-ttu-id="c4c73-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4c73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c73-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4c73-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c73-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4c73-126">INPUTS</span></span>

### <span data-ttu-id="c4c73-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c4c73-127">None</span></span>

## <span data-ttu-id="c4c73-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4c73-128">OUTPUTS</span></span>

### <span data-ttu-id="c4c73-129">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSContactDetail)</span><span class="sxs-lookup"><span data-stu-id="c4c73-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="c4c73-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4c73-130">NOTES</span></span>

## <span data-ttu-id="c4c73-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4c73-131">RELATED LINKS</span></span>
