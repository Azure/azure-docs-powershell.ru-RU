---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076477"
---
# <span data-ttu-id="2e6a8-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e6a8-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="2e6a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6a8-103">Удаление среды Azure из Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="2e6a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e6a8-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e6a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e6a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6a8-106">Командлет **Remove-AzureEnvironment** удаляет среду Azure из перемещаемого профиля, поэтому Windows PowerShell не удается найти его.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="2e6a8-107">Этот командлет не удаляет среду из Microsoft Azure или может быть изменена в реальной среде.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="2e6a8-108">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="2e6a8-109">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="2e6a8-110">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2e6a8-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="2e6a8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e6a8-111">EXAMPLES</span></span>

### <span data-ttu-id="2e6a8-112">Пример 1: Удаление среды</span><span class="sxs-lookup"><span data-stu-id="2e6a8-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="2e6a8-113">Эта команда удаляет среду ContosoEnv из Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="2e6a8-114">Пример 2: удаление нескольких сред</span><span class="sxs-lookup"><span data-stu-id="2e6a8-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="2e6a8-115">Эта команда удаляет среды, имена которых начинаются с "contoso", из Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="2e6a8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e6a8-116">PARAMETERS</span></span>

### <span data-ttu-id="2e6a8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e6a8-117">-Force</span></span>
<span data-ttu-id="2e6a8-118">Подавляет вывод запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-118">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="2e6a8-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e6a8-119">-Name</span></span>
<span data-ttu-id="2e6a8-120">Указывает имя среды, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="2e6a8-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-121">This parameter is required.</span></span>
<span data-ttu-id="2e6a8-122">Значение этого параметра учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="2e6a8-123">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-123">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="2e6a8-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="2e6a8-124">-Profile</span></span>
<span data-ttu-id="2e6a8-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2e6a8-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e6a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6a8-127">CommonParameters</span></span>
<span data-ttu-id="2e6a8-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6a8-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6a8-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e6a8-130">INPUTS</span></span>

### <span data-ttu-id="2e6a8-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="2e6a8-131">None</span></span>
<span data-ttu-id="2e6a8-132">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2e6a8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e6a8-133">OUTPUTS</span></span>

### <span data-ttu-id="2e6a8-134">None и System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e6a8-134">None or System.Boolean</span></span>
<span data-ttu-id="2e6a8-135">Если вы используете параметр *PassThru* , этот командлет возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="2e6a8-136">В противном случае он не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2e6a8-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="2e6a8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e6a8-137">NOTES</span></span>

## <span data-ttu-id="2e6a8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e6a8-138">RELATED LINKS</span></span>

[<span data-ttu-id="2e6a8-139">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e6a8-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="2e6a8-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e6a8-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="2e6a8-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2e6a8-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


