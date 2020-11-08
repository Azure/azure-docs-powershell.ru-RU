---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076154"
---
# <span data-ttu-id="1ee00-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee00-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="1ee00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ee00-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee00-103">Удаление группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="1ee00-103">Deletes a network security group.</span></span>

## <span data-ttu-id="1ee00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ee00-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ee00-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee00-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee00-106">Командлет **Remove-AzureNetworkSecurityGroup** удаляет группу безопасности сети Azure из подписки.</span><span class="sxs-lookup"><span data-stu-id="1ee00-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="1ee00-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ee00-107">EXAMPLES</span></span>

## <span data-ttu-id="1ee00-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ee00-108">PARAMETERS</span></span>

### <span data-ttu-id="1ee00-109">-Force</span><span class="sxs-lookup"><span data-stu-id="1ee00-109">-Force</span></span>
<span data-ttu-id="1ee00-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ee00-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ee00-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ee00-111">-Name</span></span>
<span data-ttu-id="1ee00-112">Указывает имя сетевой группы безопасности, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="1ee00-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1ee00-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ee00-113">-PassThru</span></span>
<span data-ttu-id="1ee00-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1ee00-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="1ee00-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1ee00-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1ee00-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="1ee00-116">-Profile</span></span>
<span data-ttu-id="1ee00-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1ee00-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1ee00-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ee00-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ee00-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee00-119">CommonParameters</span></span>
<span data-ttu-id="1ee00-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ee00-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee00-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee00-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee00-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ee00-122">INPUTS</span></span>

## <span data-ttu-id="1ee00-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee00-123">OUTPUTS</span></span>

## <span data-ttu-id="1ee00-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ee00-124">NOTES</span></span>

## <span data-ttu-id="1ee00-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ee00-125">RELATED LINKS</span></span>

[<span data-ttu-id="1ee00-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee00-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="1ee00-127">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee00-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


