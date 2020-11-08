---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075869"
---
# <span data-ttu-id="a2000-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a2000-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="a2000-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2000-102">SYNOPSIS</span></span>
<span data-ttu-id="a2000-103">Удаление правила сетевой безопасности из группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a2000-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="a2000-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2000-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2000-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2000-105">DESCRIPTION</span></span>
<span data-ttu-id="a2000-106">Командлет **Remove-AzureNetworkSecurityRule** удаляет правило сетевой безопасности Azure из группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a2000-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="a2000-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2000-107">EXAMPLES</span></span>

## <span data-ttu-id="a2000-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2000-108">PARAMETERS</span></span>

### <span data-ttu-id="a2000-109">-Force</span><span class="sxs-lookup"><span data-stu-id="a2000-109">-Force</span></span>
<span data-ttu-id="a2000-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2000-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2000-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2000-111">-Name</span></span>
<span data-ttu-id="a2000-112">Указывает имя для правила сетевой безопасности, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a2000-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2000-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2000-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a2000-114">Указывает сетевую группу безопасности, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a2000-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="a2000-115">Чтобы получить объект **INetworkSecurityGroup** , используйте командлет Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="a2000-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2000-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="a2000-116">-Profile</span></span>
<span data-ttu-id="a2000-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a2000-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a2000-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2000-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2000-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2000-119">CommonParameters</span></span>
<span data-ttu-id="a2000-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2000-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2000-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2000-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2000-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2000-122">INPUTS</span></span>

## <span data-ttu-id="a2000-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2000-123">OUTPUTS</span></span>

## <span data-ttu-id="a2000-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2000-124">NOTES</span></span>

## <span data-ttu-id="a2000-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2000-125">RELATED LINKS</span></span>

[<span data-ttu-id="a2000-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a2000-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


