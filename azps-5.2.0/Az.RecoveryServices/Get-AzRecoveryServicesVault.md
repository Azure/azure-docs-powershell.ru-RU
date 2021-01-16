---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413031"
---
# <span data-ttu-id="b100a-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b100a-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b100a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b100a-102">SYNOPSIS</span></span>

<span data-ttu-id="b100a-103">Получает список сейфов служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b100a-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="b100a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b100a-104">SYNTAX</span></span>

### <span data-ttu-id="b100a-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b100a-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b100a-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b100a-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b100a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b100a-107">DESCRIPTION</span></span>

<span data-ttu-id="b100a-108">Для **получения списка сейфов служб** восстановления в текущей подписке возвращается список хранилищ Службы восстановления.</span><span class="sxs-lookup"><span data-stu-id="b100a-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="b100a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b100a-109">EXAMPLES</span></span>

### <span data-ttu-id="b100a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b100a-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="b100a-111">Получить список сейфа в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="b100a-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="b100a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b100a-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="b100a-113">Получить список хранилища в группе ресурсов выбранной подписки.</span><span class="sxs-lookup"><span data-stu-id="b100a-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="b100a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b100a-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="b100a-115">Получить хранилище в группе ресурсов с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="b100a-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="b100a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b100a-116">PARAMETERS</span></span>

### <span data-ttu-id="b100a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b100a-117">-DefaultProfile</span></span>

<span data-ttu-id="b100a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b100a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b100a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b100a-119">-Name</span></span>

<span data-ttu-id="b100a-120">Указывает имя хранилища, для которого нужно найти запрос.</span><span class="sxs-lookup"><span data-stu-id="b100a-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b100a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b100a-121">-ResourceGroupName</span></span>

<span data-ttu-id="b100a-122">Имя группы ресурсов Azure, из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b100a-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b100a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="b100a-123">-Tag</span></span>

<span data-ttu-id="b100a-124">Указывает теги для запроса</span><span class="sxs-lookup"><span data-stu-id="b100a-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b100a-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="b100a-125">-TagName</span></span>

<span data-ttu-id="b100a-126">Ключ тега для запроса</span><span class="sxs-lookup"><span data-stu-id="b100a-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b100a-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="b100a-127">-TagValue</span></span>

<span data-ttu-id="b100a-128">Значение тега для запроса</span><span class="sxs-lookup"><span data-stu-id="b100a-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b100a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b100a-129">CommonParameters</span></span>
<span data-ttu-id="b100a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b100a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b100a-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b100a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b100a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b100a-132">INPUTS</span></span>

### <span data-ttu-id="b100a-133">Нет</span><span class="sxs-lookup"><span data-stu-id="b100a-133">None</span></span>

## <span data-ttu-id="b100a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b100a-134">OUTPUTS</span></span>

### <span data-ttu-id="b100a-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="b100a-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b100a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b100a-136">NOTES</span></span>
<span data-ttu-id="b100a-137">Get-AzRecoveryServicesVault az.RecoveryServices(<=2.10.0) не может работать с Az.Accounts(>=1.8.1) из-за неправильной ссылки на сборку.</span><span class="sxs-lookup"><span data-stu-id="b100a-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="b100a-138">Если вы используете последние учетные записи Az или Az.Accounts, модуль Az.RecoveryServices необходимо обновить до версии 2.11.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b100a-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="b100a-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b100a-139">RELATED LINKS</span></span>

[<span data-ttu-id="b100a-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b100a-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b100a-141">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b100a-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="b100a-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b100a-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
