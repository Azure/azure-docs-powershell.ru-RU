---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076334"
---
# <span data-ttu-id="96404-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96404-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="96404-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96404-102">SYNOPSIS</span></span>
<span data-ttu-id="96404-103">Получение сведений о группе безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="96404-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="96404-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96404-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="96404-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96404-105">DESCRIPTION</span></span>
<span data-ttu-id="96404-106">Командлет **Get-AzureNetworkSecurityGroup** возвращает сведения о сетевой группе безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="96404-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="96404-107">Укажите *подробный* параметр для отображения правил сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="96404-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="96404-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96404-108">EXAMPLES</span></span>

## <span data-ttu-id="96404-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96404-109">PARAMETERS</span></span>

### <span data-ttu-id="96404-110">-Подробно</span><span class="sxs-lookup"><span data-stu-id="96404-110">-Detailed</span></span>
<span data-ttu-id="96404-111">Указывает на то, что этот командлет возвращает правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="96404-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96404-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96404-112">-Name</span></span>
<span data-ttu-id="96404-113">Указывает имя сетевой группы безопасности, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="96404-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="96404-114">Если классическая Сетевая группа безопасности создана в группе ресурсов, отличной от ***сети по умолчанию*** , с помощью портала Azure, необходимо использовать следующий синтаксис PowerShell: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .</span><span class="sxs-lookup"><span data-stu-id="96404-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96404-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="96404-115">-Profile</span></span>
<span data-ttu-id="96404-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="96404-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96404-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="96404-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96404-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96404-118">CommonParameters</span></span>
<span data-ttu-id="96404-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96404-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96404-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96404-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96404-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96404-121">INPUTS</span></span>

## <span data-ttu-id="96404-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96404-122">OUTPUTS</span></span>

## <span data-ttu-id="96404-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="96404-123">NOTES</span></span>

## <span data-ttu-id="96404-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96404-124">RELATED LINKS</span></span>

[<span data-ttu-id="96404-125">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96404-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="96404-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="96404-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

