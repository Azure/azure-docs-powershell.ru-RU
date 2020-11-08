---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076084"
---
# <span data-ttu-id="e02f0-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="e02f0-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="e02f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e02f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e02f0-103">Перезапуск виртуальной машины в коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e02f0-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e02f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e02f0-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e02f0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e02f0-105">DESCRIPTION</span></span>
<span data-ttu-id="e02f0-106">Командлет **restart-AzureRemoteAppVM** перезапустит виртуальную машину в коллекции RemoteApp для Azure, к которой подключен указанный пользователь.</span><span class="sxs-lookup"><span data-stu-id="e02f0-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="e02f0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e02f0-107">EXAMPLES</span></span>

### <span data-ttu-id="e02f0-108">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e02f0-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="e02f0-109">Эта команда перезапускает виртуальную машину в коллекции Azure RemoteApp с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="e02f0-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="e02f0-110">Пользователь PattiFuller@contoso.com подключен к коллекции, содержащей эту виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e02f0-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="e02f0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e02f0-111">PARAMETERS</span></span>

### <span data-ttu-id="e02f0-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e02f0-112">-CollectionName</span></span>
<span data-ttu-id="e02f0-113">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e02f0-113">Specifies the name of an Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f0-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="e02f0-114">-LogoffMessage</span></span>
<span data-ttu-id="e02f0-115">Задает предупреждение о том, что пользователи, подключенные к виртуальной машине, не выписывают их в журнал.</span><span class="sxs-lookup"><span data-stu-id="e02f0-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f0-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="e02f0-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="e02f0-117">Указывает, как долго этот командлет ожидает, прежде чем он войдет в систему пользователей.</span><span class="sxs-lookup"><span data-stu-id="e02f0-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="e02f0-118">Значение по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="e02f0-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f0-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="e02f0-119">-Profile</span></span>
<span data-ttu-id="e02f0-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e02f0-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e02f0-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e02f0-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e02f0-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="e02f0-122">-UserUpn</span></span>
<span data-ttu-id="e02f0-123">Указывает имя участника-пользователя (UPN) пользователя, для которого этот командлет перезапускает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e02f0-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="e02f0-124">Чтобы получить доступ к виртуальным машинам в коллекции и подключенному UPN, используйте командлет **Get-AzureRemoteAppVM** .</span><span class="sxs-lookup"><span data-stu-id="e02f0-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e02f0-125">-Confirm</span></span>
<span data-ttu-id="e02f0-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e02f0-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02f0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02f0-127">-WhatIf</span></span>
<span data-ttu-id="e02f0-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e02f0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e02f0-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e02f0-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02f0-130">CommonParameters</span></span>
<span data-ttu-id="e02f0-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e02f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02f0-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02f0-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e02f0-133">INPUTS</span></span>

## <span data-ttu-id="e02f0-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e02f0-134">OUTPUTS</span></span>

## <span data-ttu-id="e02f0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e02f0-135">NOTES</span></span>

## <span data-ttu-id="e02f0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e02f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="e02f0-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="e02f0-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


